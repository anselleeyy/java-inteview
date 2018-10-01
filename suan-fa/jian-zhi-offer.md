---
description: 剑指 Offer 题解
---

# 剑指 Offer

### 1. 二维数组中的查找

#### 题目描述

> 在一个二维数组中（每个一维数组的长度相同），每一行都按照从左到右递增的顺序排序，每一列都按照从上到下递增的顺序排序。请完成一个函数，输入这样的一个二维数组和一个整数，判断数组中是否含有该整数。
>
> 链接：[https://www.nowcoder.com/practice/abc3fe2ce8e146608e868a70efebf62e?tpId=13&tqId=11154&tPage=1&rp=1&ru=/ta/coding-interviews&qru=/ta/coding-interviews/question-ranking](https://www.nowcoder.com/practice/abc3fe2ce8e146608e868a70efebf62e?tpId=13&tqId=11154&tPage=1&rp=1&ru=/ta/coding-interviews&qru=/ta/coding-interviews/question-ranking)

#### 解题思路

> 由于每行（每列）都是递增的，所以可以使用从右上往左下逼近的方法找到这个值。
>
> 当前值大于target则左移一列，小于target则下移一行

```javascript
public class Solution {
    public boolean Find(int target, int [][] array) {
        boolean ifFound = false;
        int row = array.length;
        int column = array[0].length;
        if (row >= 0 && column >= 0) {
            int ro = 0;
            int col = column-1;
            while (ro < row && col >= 0) {
                if (array[ro][col] > target) {
                    col--;
                } else if (array[ro][col] == target) {
                    ifFound = true;
                    break;
                } else ro++;
            }
        }
        return ifFound;
    }
}
```

### 2. 替换空格

#### 题目描述

> 请实现一个函数，将一个字符串中的每个空格替换成“%20”。例如，当字符串为We Are Happy.则经过替换之后的字符串为We%20Are%20Happy
>
> 题目链接：[https://www.nowcoder.com/practice/4060ac7e3e404ad1a894ef3e17650423?tpId=13&tqId=11155&tPage=1&rp=1&ru=%2Fta%2Fcoding-interviews&qru=%2Fta%2Fcoding-interviews%2Fquestion-ranking](https://www.nowcoder.com/practice/4060ac7e3e404ad1a894ef3e17650423?tpId=13&tqId=11155&tPage=1&rp=1&ru=%2Fta%2Fcoding-interviews&qru=%2Fta%2Fcoding-interviews%2Fquestion-ranking)

#### 解题思路

> 思路1：暴力遍历整个字符串，额外建立空间给 String result，使用拼接的做法。该方法的时间和空间复杂度均为：O\(n\)
>
> 思路2：遍历两次，第一次记录空格的个数，有空格就扩展str的长度（+2），第二次从后往前遍历，通过两个指针，一个指向原来的str，一个指向新的str，如果遇到空格则添加3个字符，否则添加当前的字符。达到原地算法。

```javascript
public class Solution {
    public String replaceSpace(StringBuffer str) {
        int i = str.length() - 1;
        for (int t = 0; t <= i; t++) {
            if (str.charAt(t) == ' ') {
                str.append("  ");
            }
        }
        int j = str.length() - 1;
        while (i >= 0 && j >= i) {
            char tmp = str.charAt(i--);
            if (tmp == ' ') {
                str.setCharAt(j--, '0');
                str.setCharAt(j--, '2');
                str.setCharAt(j--, '%');
            } else {
                str.setCharAt(j--, tmp);
            }
        }
        return str.toString();
    }
}
```

### 3.  从尾到头打印链表

#### 题目描述

> 输入一个链表，按链表值从尾到头的顺序返回一个ArrayList
>
> 题目链接：[https://www.nowcoder.com/practice/d0267f7f55b3412ba93bd35cfa8e8035?tpId=13&tqId=11156&tPage=1&rp=1&ru=%2Fta%2Fcoding-interviews&qru=%2Fta%2Fcoding-interviews%2Fquestion-ranking](https://www.nowcoder.com/practice/d0267f7f55b3412ba93bd35cfa8e8035?tpId=13&tqId=11156&tPage=1&rp=1&ru=%2Fta%2Fcoding-interviews&qru=%2Fta%2Fcoding-interviews%2Fquestion-ranking)

#### 解题思路

_**借助栈**_

```javascript
public class Solution {
    public ArrayList<Integer> printListFromTailToHead(ListNode listNode) {
        Stack<Integer> stack = new Stack<>();
        while (listNode != null) {
            stack.push(listNode.val);
            listNode = listNode.next;
        }
        ArrayList<Integer> result = new ArrayList<>();
        while (!stack.isEmpty()) {
            result.add(stack.pop());
        }
        return result;
    }
}
```

_**使用递归的方式**_

```javascript
public class Solution {
    public ArrayList<Integer> printListFromTailToHead(ListNode listNode) {
        ArrayList<Integer> result = new ArrayList<>();
        if (listNode == null) return result;
        result.addAll(printListFromTailToHead(listNode.next));
        result.add(listNode.val);
        return result;
    }
}
```

_**借助链表原地反转的思想**_

```javascript
public class Solution {
    public ArrayList<Integer> printListFromTailToHead(ListNode listNode) {
        ArrayList<Integer> result = new ArrayList<>();
        if (listNode == null) return result;
        if (listNode.next == null) {
            result.add(listNode.val);
            return result;
        }
        ListNode pre = null;
        ListNode next = null;
        while (listNode != null) {
            next = listNode.next;
            listNode.next = pre;
            pre = listNode;
            listNode = next;
        }
        while (pre != null) {
            result.add(pre.val);
            pre = pre.next;
        }
        return result;
    }
}
```

### 4. 重建二叉树

#### 题目描述

> 输入某二叉树的前序遍历和中序遍历的结果，请重建出该二叉树。假设输入的前序遍历和中序遍历的结果中都不含重复的数字。例如输入前序遍历序列{1,2,4,7,3,5,6,8}和中序遍历序列{4,7,2,1,5,3,8,6}，则重建二叉树并返回
>
> 题目链接：[https://www.nowcoder.com/practice/8a19cbe657394eeaac2f6ea9b0f6fcf6?tpId=13&tqId=11157&tPage=1&rp=1&ru=%2Fta%2Fcoding-interviews&qru=%2Fta%2Fcoding-interviews%2Fquestion-ranking](https://www.nowcoder.com/practice/8a19cbe657394eeaac2f6ea9b0f6fcf6?tpId=13&tqId=11157&tPage=1&rp=1&ru=%2Fta%2Fcoding-interviews&qru=%2Fta%2Fcoding-interviews%2Fquestion-ranking)

#### 解题思路

> 根据前序遍历的特点，我们可以通过第一个值得到当前子树的根节点，借此去中序遍历查找根节点的左子树和右子树，采用递归的思路

```javascript
public class Solution {
    public TreeNode reConstructBinaryTree(int [] pre,int [] in) {
        // 获取根节点
        int val = pre[0];
        TreeNode root = new TreeNode(val);
        // 得到左子树的大小
        int len = 0;
        for (; len < in.length; len++) {
            if (in[len] == val) break;
        }
        // 构建左子树
        if (len != 0) {
            // 左子树的先序遍历
            int[] pre_left = new int[len];
            for (int i = 0; i < len; i++) {
                pre_left[i] = pre[i+1];
            }
            // 左子树的中序遍历
            int[] in_left = new int[len];
            for (int i = 0; i < len; i++) {
                in_left[i] = in[i];
            }
            root.left = reConstructBinaryTree(pre_left, in_left);
        }
        
        // 构建右子树
        if (len != (pre.length-1)) {
            // 右子树的先序遍历
            int[] pre_right = new int[pre.length-len-1];
            for (int i = 0, idx = len+1; idx < pre.length; i++, idx++) {
                pre_right[i] = pre[idx];
            }
            // 右子树的中序遍历
            int[] in_right = new int[in.length-len-1];
            for (int i = 0, idx = len+1; idx < in.length; i++, idx++) {
                in_right[i] = in[idx];
            }
            root.right = reConstructBinaryTree(pre_right, in_right);
        }
        return root;
    }
}
```

### 15. 反转链表

#### 题目描述

> 输入一个链表，反转链表后，输出新链表的表头
>
> 题目链接：[https://www.nowcoder.com/practice/75e878df47f24fdc9dc3e400ec6058ca?tpId=13&tqId=11168&tPage=1&rp=1&ru=%2Fta%2Fcoding-interviews&qru=%2Fta%2Fcoding-interviews%2Fquestion-ranking](https://www.nowcoder.com/practice/75e878df47f24fdc9dc3e400ec6058ca?tpId=13&tqId=11168&tPage=1&rp=1&ru=%2Fta%2Fcoding-interviews&qru=%2Fta%2Fcoding-interviews%2Fquestion-ranking)

#### 解题思路

> 思路1：借助栈
>
> 思路2：递归
>
> 思路3：链表原地反转

```javascript
public class Solution {
    public ListNode ReverseList(ListNode head) {
        if (head == null || head.next == null) return head;
        ListNode pre = null;
        ListNode next = null;
        while (head != null) {
            next = head.next;
            head.next = pre;
            pre = head;
            head = next;
        }
        return pre;
    }
}
```



