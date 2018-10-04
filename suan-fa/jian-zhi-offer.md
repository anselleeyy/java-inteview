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

### 5. 用两个栈实现队列

#### 题目描述

> 用两个栈来实现一个队列，完成队列的Push和Pop操作。 队列中的元素为int类型
>
> 题目链接：[https://www.nowcoder.com/practice/54275ddae22f475981afa2244dd448c6?tpId=13&tqId=11158&tPage=1&rp=1&ru=%2Fta%2Fcoding-interviews&qru=%2Fta%2Fcoding-interviews%2Fquestion-ranking](https://www.nowcoder.com/practice/54275ddae22f475981afa2244dd448c6?tpId=13&tqId=11158&tPage=1&rp=1&ru=%2Fta%2Fcoding-interviews&qru=%2Fta%2Fcoding-interviews%2Fquestion-ranking)

#### 解题思路

> 利用栈的先进后出思想，两个栈配合达到先进先出

```javascript
public class Solution {
    Stack<Integer> stack1 = new Stack<Integer>();
    Stack<Integer> stack2 = new Stack<Integer>();
    
    public void push(int node) {
        stack1.push(node);
    }
    
    public int pop() {
        if (stack2.isEmpty()) {
            while (!stack1.isEmpty()) {
                stack2.push(stack1.pop());
            }
        }
        return stack2.pop();
    }
}
```

### 6. 旋转数组的最小数字

#### 题目描述

> 把一个数组最开始的若干个元素搬到数组的末尾，我们称之为数组的旋转。输入一个非减排序的数组的一个旋转，输出旋转数组的最小元素。
>
> 例如数组 {3, 4, 5, 1, 2} 为 { 1, 2, 3, 4, 5 } 的一个旋转，该数组的最小值为1。
>
> NOTE：给出的所有元素都大于0，若数组大小为0，请返回0。
>
> 题目链接：[https://www.nowcoder.com/practice/9f3231a991af4f55b95579b44b7a01ba?tpId=13&tqId=11159&tPage=1&rp=1&ru=%2Fta%2Fcoding-interviews&qru=%2Fta%2Fcoding-interviews%2Fquestion-ranking](https://www.nowcoder.com/practice/9f3231a991af4f55b95579b44b7a01ba?tpId=13&tqId=11159&tPage=1&rp=1&ru=%2Fta%2Fcoding-interviews&qru=%2Fta%2Fcoding-interviews%2Fquestion-ranking)

#### 解题思路

> 二分思想：数组变成了两段升序的子序列，每一次找中间点，如果中间点大于最后边的，代表转折点在中间点和右端之间，否则在左端

```javascript
public class Solution {
    public int minNumberInRotateArray(int [] array) {
        int i = 0;
        int j = array.length-1;
        if (i == j) return 0;
        int middle = 0;
        while (array[i] >= array[j]) {
            if (j - i == 1) {
                middle = j;
                break;
            }
            middle = i + (j - i) / 2;
            if (array[middle] >= array[j]) {
                i = middle;
            } else {
                j = middle;
            }
        }
        return array[middle];
    }
}
```

### 7. 斐波那契数列

#### 题目描述

> 大家都知道斐波那契数列，现在要求输入一个整数n，请你输出斐波那契数列的第n项（从0开始，第0项为0，n &lt;= 39）
>
> 题目链接：[https://www.nowcoder.com/practice/c6c7742f5ba7442aada113136ddea0c3?tpId=13&tqId=11160&tPage=1&rp=1&ru=%2Fta%2Fcoding-interviews&qru=%2Fta%2Fcoding-interviews%2Fquestion-ranking](https://www.nowcoder.com/practice/c6c7742f5ba7442aada113136ddea0c3?tpId=13&tqId=11160&tPage=1&rp=1&ru=%2Fta%2Fcoding-interviews&qru=%2Fta%2Fcoding-interviews%2Fquestion-ranking)

#### 解题思路

> 迭代或递归思路，但由于 n 较大，递归会爆栈

```javascript
public class Solution {
    public int Fibonacci(int n) {
        if (n == 0) return 0;
        if (n == 1 || n == 2) return 1;
        int[] result = new int[n+1];
        result[1] = 1;
        result[2] = 1;
        for (int i = 3; i < n+1; i++) {
            result[i] = result[i-1] + result[i-2];
        }
        return result[n];
    }
}
```

### 8. 跳台阶

#### 题目描述

> 一只青蛙一次可以跳上1级台阶，也可以跳上2级。求该青蛙跳上一个n级的台阶总共有多少种跳法（先后次序不同算不同的结果）。

#### 解题思路

> 动态规划：第 n\(n &gt;= 3\) 级的台阶可以通过青蛙在 n-1 级跳一级或 n-2 级跳两级达到

```javascript
public class Solution {
    public int JumpFloor(int target) {
        if (target <= 2) return target;
        int[] result = new int[target+1];
        result[1] = 1;
        result[2] = 2;
        for (int i = 3; i <= target; i++) {
            result[i] = result[i-1] + result[i-2];
        }
        return result[target];
    }
}
```

### 9. 变态跳台阶

#### 题目描述

> 一只青蛙一次可以跳上1级台阶，也可以跳上2级……它也可以跳上n级。求该青蛙跳上一个n级的台阶总共有多少种跳法

#### 解题思路

> 公式法：F\(n\) = F\(n-1\)+F\(n-2\)+F\(n-3\)+...+F\(1\)，F\(n-1\) = F\(n-2\)+F\(n-3\)+...+F\(1\) =&gt; F\(n\) = 2 \* F\(n-1\)
>
> 在网上看到这种说法，感觉更加易懂：每个台阶都有跳与不跳两种情况（除了最后一个台阶），最后一个台阶必须跳。所以共用 2^\(n-1\) 中情况

```javascript
public class Solution {
    public int JumpFloorII(int target) {
        if (target == 0) return 0;
        // return (int) Math.pow(2, target-1);
        return 1 << (target-1);  // 位移操作，更快
    }
}
```

### 10. 矩阵覆盖

#### 题目描述

> 我们可以用2\*1的小矩形横着或者竖着去覆盖更大的矩形。请问用n个2\*1的小矩形无重叠地覆盖一个2\*n的大矩形，总共有多少种方法？
>
> 题目链接：[https://www.nowcoder.com/practice/72a5a919508a4251859fb2cfb987a0e6?tpId=13&tqId=11163&tPage=1&rp=1&ru=%2Fta%2Fcoding-interviews&qru=%2Fta%2Fcoding-interviews%2Fquestion-ranking](https://www.nowcoder.com/practice/72a5a919508a4251859fb2cfb987a0e6?tpId=13&tqId=11163&tPage=1&rp=1&ru=%2Fta%2Fcoding-interviews&qru=%2Fta%2Fcoding-interviews%2Fquestion-ranking)

#### 解题思路

> 同第8题跳台阶相同

```javascript
public class Solution {
    public int RectCover(int target) {
        if (target <= 2) return target;
        int[] result = new int[target+1];
        result[1] = 1;
        result[2] = 2;
        for (int i = 3; i <= target; i++) {
            result[i] = result[i-1] + result[i-2];
        }
        return result[target];
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



