# 剑指 Offer

## 目录

- [1 二维数组中的查找](剑指%20Offer%20题解.md#1-二维数组中的查找)
- [2 替换空格](剑指%20Offer%20题解.md#2-替换空格)
- [3 从尾到头打印链表](剑指%20Offer%20题解.md#3-从尾到头打印链表)
- [4 重建二叉树](剑指%20Offer%20题解.md#4-重建二叉树)
- [5 用两个栈实现队列](剑指%20Offer%20题解.md#5-用两个栈实现队列)
- [6 旋转数组的最小数字](剑指%20Offer%20题解.md#6-旋转数组的最小数字)
- [7 斐波那契数列](剑指%20Offer%20题解.md#7-斐波那契数列)
- [8 跳台阶](剑指%20Offer%20题解.md#8-跳台阶)
- [9 变态跳台阶](剑指%20Offer%20题解.md#9-变态跳台阶)
- [10 矩阵覆盖](剑指%20Offer%20题解.md#10-矩阵覆盖)
- [11 二进制中1的个数](剑指%20Offer%20题解.md#11-二进制中1的个数)
- [12 数值的整数次方](剑指%20Offer%20题解.md#12-数值的整数次方)
- [13 调整数组顺序使奇数位于偶数前面](剑指%20Offer%20题解.md#13-调整数组顺序使奇数位于偶数前面)
- [14 链表中倒数第k个结点](剑指%20Offer%20题解.md#14-链表中倒数第k个结点)
- [15 反转链表](剑指%20Offer%20题解.md#15-反转链表)
- [16 合并两个排序链表](剑指%20Offer%20题解.md#16-合并两个排序链表)
- [17 树的子结构](剑指%20Offer%20题解.md#17-树的子结构)
- [18 二叉树的镜像](剑指%20Offer%20题解.md#18-二叉树的镜像)
- [19 顺时针打印矩阵](剑指%20Offer%20题解.md#19-顺时针打印矩阵)
- [20 包含min函数的栈](剑指%20Offer%20题解.md#20-包含min函数的栈)
- [21 栈的压入、弹出序列](剑指%20Offer%20题解.md#21-栈的压入、弹出序列)
- [22 从上往下打印二叉树](剑指%20Offer%20题解.md#22-从上往下打印二叉树)
- [23 二叉搜索树的后序遍历序列](剑指%20Offer%20题解.md#23-二叉搜索树的后序遍历序列)
- [24 二叉树中和为某一值的路径](剑指%20Offer%20题解.md#24-二叉树中和为某一值的路径)
- [25 复杂链表的复制](剑指%20Offer%20题解.md#25-复杂链表的复制)
- [26 二叉搜索树与双向链表](剑指%20Offer%20题解.md#26-二叉搜索树与双向链表)
- [27 字符串的排列](剑指%20Offer%20题解.md#27-字符串的排列)
- [28 数组中出现次数超过一半的数字](剑指%20Offer%20题解.md#28-数组中出现次数超过一半的数字)
- [29 最小的 k 个数](剑指%20Offer%20题解.md#29-最小的k个数)
- [30 连续子数组的最大和](剑指%20Offer%20题解.md#30-连续子数组的最大和)
- [31 整数中1出现的次数（从1到n整数中1出现的次数）](剑指%20Offer%20题解.md#31-整数中1出现的次数（从1到n整数中1出现的次数）)
- [32 把数组排成最小的数](剑指%20Offer%20题解.md#32-把数组排成最小的数)
- [33 丑数](剑指%20Offer%20题解.md#33-丑数)
- [34 第一个只出现一次的字符位置](剑指%20Offer%20题解.md#34-第一个只出现一次的字符位置)
- [35 数组中的逆序对](剑指%20Offer%20题解.md#35-数组中的逆序对)
- [36 两个链表的第一个公共结点](剑指%20Offer%20题解.md#36-两个链表的第一个公共结点)
- [37 数字在排序数组中出现的次数](剑指%20Offer%20题解.md#37-数字在排序数组中出现的次数)
- [38 二叉树的深度](剑指%20Offer%20题解.md#38-二叉树的深度)
- [39 平衡二叉树](剑指%20Offer%20题解.md#39-平衡二叉树)
- [40 数组中只出现一次的数字](剑指%20Offer%20题解.md#40-数组中只出现一次的数字)
- [41 和为S的连续正数序列](剑指%20Offer%20题解.md#41-和为S的连续正数序列)
- [42 和为S的两个数字](剑指%20Offer%20题解.md#42-和为S的两个数字)
- [43 左旋转字符串](剑指%20Offer%20题解.md#43-左旋转字符串)

## 题册

### 1. 二维数组中的查找

#### 题目描述

> 在一个二维数组中（每个一维数组的长度相同），每一行都按照从左到右递增的顺序排序，每一列都按照从上到下递增的顺序排序。请完成一个函数，输入这样的一个二维数组和一个整数，判断数组中是否含有该整数。
>
> 链接：[https://www.nowcoder.com/practice/abc3fe2ce8e146608e868a70efebf62e](https://www.nowcoder.com/practice/abc3fe2ce8e146608e868a70efebf62e)

#### 解题思路

> 由于每行（每列）都是递增的，所以可以使用从右上往左下逼近的方法找到这个值。
>
> 当前值大于target则左移一列，小于target则下移一行

```java
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
> 题目链接：[https://www.nowcoder.com/practice/4060ac7e3e404ad1a894ef3e17650423](https://www.nowcoder.com/practice/4060ac7e3e404ad1a894ef3e17650423)

#### 解题思路

> 思路1：暴力遍历整个字符串，额外建立空间给 String result，使用拼接的做法。该方法的时间和空间复杂度均为：O\(n\)
>
> 思路2：遍历两次，第一次记录空格的个数，有空格就扩展str的长度（+2），第二次从后往前遍历，通过两个指针，一个指向原来的str，一个指向新的str，如果遇到空格则添加3个字符，否则添加当前的字符。达到原地算法。

```java
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

### 3. 从尾到头打印链表

#### 题目描述

> 输入一个链表，按链表值从尾到头的顺序返回一个ArrayList
>
> 题目链接：[https://www.nowcoder.com/practice/d0267f7f55b3412ba93bd35cfa8e8035](https://www.nowcoder.com/practice/d0267f7f55b3412ba93bd35cfa8e8035)

#### 解题思路

_**借助栈**_

```java
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

```java
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

```java
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
> 题目链接：[https://www.nowcoder.com/practice/8a19cbe657394eeaac2f6ea9b0f6fcf6](https://www.nowcoder.com/practice/8a19cbe657394eeaac2f6ea9b0f6fcf6)

#### 解题思路

> 根据前序遍历的特点，我们可以通过第一个值得到当前子树的根节点，借此去中序遍历查找根节点的左子树和右子树，采用递归的思路

```java
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
> 题目链接：[https://www.nowcoder.com/practice/54275ddae22f475981afa2244dd448c6](https://www.nowcoder.com/practice/54275ddae22f475981afa2244dd448c6)

#### 解题思路

> 利用栈的先进后出思想，两个栈配合达到先进先出

```java
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
> 题目链接：[https://www.nowcoder.com/practice/9f3231a991af4f55b95579b44b7a01ba](https://www.nowcoder.com/practice/9f3231a991af4f55b95579b44b7a01ba)

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
> 题目链接：[https://www.nowcoder.com/practice/c6c7742f5ba7442aada113136ddea0c3](https://www.nowcoder.com/practice/c6c7742f5ba7442aada113136ddea0c3)

#### 解题思路

> 迭代或递归思路，但由于 n 较大，递归会爆栈

```java
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

> 一只青蛙一次可以跳上1级台阶，也可以跳上2级。求该青蛙跳上一个n级的台阶总共有多少种跳法（先后次序不同算不同的结果）
> 
> 题目链接：[https://www.nowcoder.com/practice/8c82a5b80378478f9484d87d1c5f12a4](https://www.nowcoder.com/practice/8c82a5b80378478f9484d87d1c5f12a4)

#### 解题思路

> 动态规划：第 n(n &gt;= 3) 级的台阶可以通过青蛙在 n-1 级跳一级或 n-2 级跳两级达到

```java
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
> 
> 题目链接：[https://www.nowcoder.com/practice/22243d016f6b47f2a6928b4313c85387](https://www.nowcoder.com/practice/22243d016f6b47f2a6928b4313c85387)

#### 解题思路

> 公式法：F(n) = F(n-1)+F(n-2)+F(n-3)+...+F(1)，F(n-1) = F(n-2)+F(n-3)+...+F(1) =&gt; F(n) = 2 * F(n-1)
>
> 在网上看到这种说法，感觉更加易懂：每个台阶都有跳与不跳两种情况（除了最后一个台阶），最后一个台阶必须跳。所以共用 2^(n-1) 种情况

```java
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
> 题目链接：[https://www.nowcoder.com/practice/72a5a919508a4251859fb2cfb987a0e6](https://www.nowcoder.com/practice/72a5a919508a4251859fb2cfb987a0e6)

#### 解题思路

> 同第8题跳台阶相同

```java
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

### 11. 二进制中1的个数

#### 题目描述

> 输入一个整数，输出该数二进制表示中1的个数。其中负数用补码表示
> 
> 题目链接：[https://www.nowcoder.com/practice/8ee967e43c2c4ec193b040ea7fbb10b8](https://www.nowcoder.com/practice/8ee967e43c2c4ec193b040ea7fbb10b8)

#### 解题思路

> 位移 + 与 1 判断

```java
public class Solution {
    public int NumberOf1(int n) {
        int count = 0;
        while (n != 0) {
            if ((n & 1) == 1) count++;
            n >>>= 1;
        }
        return count;
    }
}
```

### 12. 数值的整数次方

#### 题目描述

> 给定一个double类型的浮点数base和int类型的整数exponent。求base的exponent次方
> 
> 题目链接：[https://www.nowcoder.com/practice/1a834e5e3e1a4b7ba251417554e07c00](https://www.nowcoder.com/practice/1a834e5e3e1a4b7ba251417554e07c00)

```java
public class Solution {
    public double Power(double base, int exponent) {
        int r = Math.abs(exponent);
        double temp = 1.0;
        while (r > 0) {
            temp *= base;
            base *= base;
            r = r >> 1;
        }
        return exponent >= 0 ? temp : 1/temp;
    }
}
```

### 13. 调整数组顺序使奇数位于偶数前面

#### 题目描述

> 输入一个整数数组，实现一个函数来调整该数组中数字的顺序，使得所有的奇数位于数组的前半部分，所有的偶数位于数组的后半部分，并保证奇数和奇数，偶数和偶数之间的相对位置不变
> 
> 题目链接：[https://www.nowcoder.com/practice/beb5aa231adc45b2a5dcc5b62c93f593](https://www.nowcoder.com/practice/beb5aa231adc45b2a5dcc5b62c93f593)

```java
public class Solution {
    public void reOrderArray(int [] array) {
        int len = array.length;
        int[] result = new int[len];
        int idx = 0;
        for (int i = 0; i < len; i++) {
            if (array[i] % 2 == 1) result[idx++] = array[i];
        }
        for (int i = 0; i < len; i++) {
            if (array[i] % 2 == 0) result[idx++] = array[i];
        }
        for (int i = 0; i < len; i++) {
            array[i] = result[i];
        }
    }
}
```

### 14. 链表中倒数第k个结点

#### 题目描述

> 输入一个链表，输出该链表中倒数第k个结点
>
> 题目链接：[https://www.nowcoder.com/practice/529d3ae5a407492994ad2a246518148a](https://www.nowcoder.com/practice/529d3ae5a407492994ad2a246518148a)

```java
public class Solution {
    public ListNode FindKthToTail(ListNode head,int k) {
        if (head == null) return head;
        ListNode first = head;
        ListNode sec = head;
        for (int i = 0; i < k; i++) {
            sec = sec.next;
            if (sec == null && i != (k-1)) return null;
        }
        // 要的是正数第一个
        if (sec == null) return head;
        // 否则
        while (sec != null) {
            first = first.next;
            sec = sec.next;
        }
        return first;
    }
}
```

### 15. 反转链表

#### 题目描述

> 输入一个链表，反转链表后，输出新链表的表头
>
> 题目链接：[https://www.nowcoder.com/practice/75e878df47f24fdc9dc3e400ec6058ca](https://www.nowcoder.com/practice/75e878df47f24fdc9dc3e400ec6058ca)

#### 解题思路

> 思路1：借助栈
>
> 思路2：递归
>
> 思路3：链表原地反转

```java
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

### 16. 合并两个排序链表

#### 题目描述

> 输入两个单调递增的链表，输出两个链表合成后的链表，当然我们需要合成后的链表满足单调不减规则
> 
> 题目链接：[https://www.nowcoder.com/practice/d8b6b4358f774294a89de2a6ac4d9337](https://www.nowcoder.com/practice/d8b6b4358f774294a89de2a6ac4d9337)

```java
public class Solution {
    public ListNode Merge(ListNode list1, ListNode list2) {
        if (list1 == null) return list2;
        if (list2 == null) return list1;
        // 递归
        ListNode head = null;
        ListNode current = null;
        while (list1 != null && list2 != null) {
            if (list1.val <= list2.val) {
                if (head == null) {
                    head = current = list1;
                } else {
                    current.next = list1;
                    current = current.next;
                }
                list1 = list1.next;
            } else {
                if (head == null) {
                    head = current = list2;
                } else {
                    current.next = list2;
                    current = current.next;
                }
                list2 = list2.next;
            }
        }
        if (list1 == null) current.next = list2;
        else current.next = list1;
        return head;
    }
}
```

### 17. 树的子结构

#### 题目描述

> 输入两棵二叉树A，B，判断B是不是A的子结构。（ps：我们约定空树不是任意一个树的子结构）
> 
> 题目链接：[https://www.nowcoder.com/practice/6e196c44c7004d15b1610b9afca8bd88](https://www.nowcoder.com/practice/6e196c44c7004d15b1610b9afca8bd88)

#### 解题思路

> 递归A树的左右子树，当遇到根节点同B树相同的，进行判断

```java
public class Solution {
    public boolean HasSubtree(TreeNode root1, TreeNode root2) {
        if (root1 == null || root2 == null) return false;
        boolean result = false;
        if (root1.val == root2.val) {
            result = check(root1, root2);
        }
        if (!result) {
            result = HasSubtree(root1.left, root2);
        }
        if (!result) {
            result = HasSubtree(root1.right, root2);
        }
        return result;
    }
    
    private boolean check(TreeNode node1, TreeNode node2) {
        if (node2 == null) return true;
        if (node1 == null) return false;
        if (node1.val != node2.val) return false;
        boolean result = true;
        result = check(node1.left, node2.left) && check(node1.right, node2.right);
        return result;
    }
}
```

### 18. 二叉树的镜像

#### 题目描述

> 操作给定的二叉树，将其变换为源二叉树的镜像
> 
> 题目链接：[https://www.nowcoder.com/practice/564f4c26aa584921bc75623e48ca3011](https://www.nowcoder.com/practice/564f4c26aa584921bc75623e48ca3011)

#### 解题思路

> 递归，可以参考 leetcode-226 翻转二叉树

```java
public class Solution {
    public void Mirror(TreeNode root) {
        if (root == null) {
            return;
        }
        TreeNode tmp = null;
        if (root != null) {
            tmp = root.left;
            root.left = root.right;
            root.right = tmp;
            if (root.left != null) {
                Mirror(root.left);
            }
            if (root.right != null) {
                Mirror(root.right);
            }
        }
    }
}
```

### 19. 顺时针打印矩阵

#### 题目描述

> 输入一个矩阵，按照从外向里以顺时针的顺序依次打印出每一个数字，例如，如果输入如下4 X 4矩阵： 
> 1 2 3 4
> 5 6 7 8
> 9 10 11 12
> 13 14 15 16 
> 则依次打印出数字：1,2,3,4,8,12,16,15,14,13,9,5,6,7,11,10
> 
> 题目链接：[https://www.nowcoder.com/practice/9b4c81a02cd34f76be2659fa0d54342a](https://www.nowcoder.com/practice/9b4c81a02cd34f76be2659fa0d54342a)

```java
// 模拟
public class Solution {
    public ArrayList<Integer> printMatrix(int [][] matrix) {
        int left = 0;
        int right = matrix[0].length - 1;
        int top = 0;
        int bottom = matrix.length - 1;
        ArrayList<Integer> result = new ArrayList<>();
        if (right < 0 || bottom < 0) return result;
        while (left <= right && top <= bottom) {
            for (int i = left; i <= right; i++) {
                result.add(matrix[top][i]);
            }
            for (int i = top+1; i <= bottom; i++) {
                result.add(matrix[i][right]);
            }
            if (top != bottom) {
            	for (int i = right-1; i >= left; i--) {
                    result.add(matrix[bottom][i]);
                }
			}
            if (left != right) {
                for (int i = bottom-1; i >= top+1; i--) {
                    result.add(matrix[i][left]);
                }
            }
            left++;
            right--;
            top++;
            bottom--;
        }
        return result;
    }
}
```

### 20. 包含 min 函数的栈

#### 题目描述

> 定义栈的数据结构，请在该类型中实现一个能够得到栈中所含最小元素的min函数（时间复杂度应为O（1））
>
> 题目链接：[https://www.nowcoder.com/practice/4c776177d2c04c2494f2555c9fcc1e49](https://www.nowcoder.com/practice/4c776177d2c04c2494f2555c9fcc1e49)

```java
public class Solution {

    private int size;
    private int min = Integer.MAX_VALUE;
    private Stack<Integer> stack = new Stack<>();
    private Integer[] elements = new Integer[10];
    
    public void push(int node) {
        ensureCapacity(size+1);
        elements[size++] = node;
        if (node < min) {
            stack.push(node);
            min = node;
        } else {
            stack.push(min);
        }
    }
    
    private void ensureCapacity(int size) {
        int len = elements.length;
        if (size > len) {
            int newLen = (len * 3) / 2 + 1;
            elements = Arrays.copyOf(elements, newLen);
        }
    }
    
    public void pop() {
        Integer top = top();
        if (top != null) {
            elements[size-1] = null;
            size--;
            stack.pop();
            min = stack.peek();
        }
    }
    
    public int top() {
        if (size != 0) {
            if (size - 1 >= 0) {
                return elements[size-1];
            }
        }
        return (Integer) null;
    }
    
    public int min() {
        return min;
    }
}
```

### 21. 栈的压入、弹出序列

#### 题目描述

> 输入两个整数序列，第一个序列表示栈的压入顺序，请判断第二个序列是否可能为该栈的弹出顺序。假设压入栈的所有数字均不相等。例如序列1,2,3,4,5是某栈的压入顺序，序列4,5,3,2,1是该压栈序列对应的一个弹出序列，但4,3,5,1,2就不可能是该压栈序列的弹出序列。（注意：这两个序列的长度是相等的）
>
> 题目链接：[https://www.nowcoder.com/practice/d77d11405cc7470d82554cb392585106](https://www.nowcoder.com/practice/d77d11405cc7470d82554cb392585106)

```java
public class Solution {
    public boolean IsPopOrder(int [] pushA, int [] popA) {
        // 借助辅助栈，模拟入栈出栈
        Stack<Integer> stack = new Stack<>();
        int j = 0, i = 0;
        for (i = 0; i < pushA.length; i++) {
            stack.push(pushA[i]);
            while (!stack.isEmpty()) {
                if (popA[j] == stack.peek()) {
                    j++;
                    stack.pop();
                } else break;
            }
        }
        if (j == popA.length && stack.isEmpty()) return true;
        return false;
    }
}
```

### 22. 从上往下打印二叉树

#### 题目描述

> 从上往下打印出二叉树的每个节点，同层节点从左至右打印
> 
> 题目链接：[https://www.nowcoder.com/practice/7fe2212963db4790b57431d9ed259701](https://www.nowcoder.com/practice/7fe2212963db4790b57431d9ed259701)

#### 解题思路

> 取出每层每个节点，输出值同时存储存在的左右子节点，进而进行层序遍历
> 
> 类似题目：[Leetcode-103 二叉树的锯齿形层次遍历](https://leetcode-cn.com/problems/binary-tree-zigzag-level-order-traversal/description/)

```java
public class Solution {
    public ArrayList<Integer> PrintFromTopToBottom(TreeNode root) { 
        ArrayList<TreeNode> list = new ArrayList<>();
        ArrayList<Integer> result = new ArrayList<>();
        if (root == null) return result;
        list.add(root);
        while (list.size() != 0) {
            TreeNode node = list.remove(0);
            result.add(node.val);
            if (node.left != null) list.add(node.left);
            if (node.right != null) list.add(node.right);
        }
        return result;
    }
}
```

### 23. 二叉搜索树的后序遍历序列

#### 题目描述

> 输入一个整数数组，判断该数组是不是某二叉搜索树的后序遍历的结果。如果是则输出Yes,否则输出No。假设输入的数组的任意两个数字都互不相同
> 
> 题目链接：[https://www.nowcoder.com/practice/a861533d45854474ac791d90e447bafd](https://www.nowcoder.com/practice/a861533d45854474ac791d90e447bafd)

#### 解题思路

> 二叉搜索树，根的左边都比根小，根的右边都比根大
> 依据上述特性，删除根节点，进而将序列分段，分段成功则继续递归

```java
public class Solution {
    public boolean VerifySquenceOfBST(int [] sequence) {
        if (sequence == null || sequence.length == 0) return false;
        int len = sequence.length;
        int i = 0;
        while (len > 1) {
            len--;
            while (sequence[i++] < sequence[len] && i < len);
            while (sequence[i++] > sequence[len] && i < len);
            if (i < len) return false;
            i = 0;
        }
        return true;
    }
}
```

### 24. 二叉树中和为某一值的路径

#### 题目描述

> 输入一颗二叉树的跟节点和一个整数，打印出二叉树中结点值的和为输入整数的所有路径。路径定义为从树的根结点开始往下一直到叶结点所经过的结点形成一条路径。(注意: 在返回值的list中，数组长度大的数组靠前)
> 
> 题目链接：[https://www.nowcoder.com/practice/b736e784e3e34731af99065031301bca](https://www.nowcoder.com/practice/b736e784e3e34731af99065031301bca)

```java
public class Solution {
	ArrayList<ArrayList<Integer>> result = new ArrayList<>();
    public ArrayList<ArrayList<Integer>> FindPath(TreeNode root, int target) {
        
        if (root == null) {
            return result;
        }
        int root_val = root.val;
        ArrayList<Integer> list = new ArrayList<>();
        list.add(root_val);
        rec(root, list, root_val, target);
        Collections.sort(result, (o1, o2) -> o2.size() - o1.size());
        return result;
    }
    
    private void rec(TreeNode node, ArrayList<Integer> list, int sum, int target) {
        if (node.left == null && node.right == null) {
            if (sum == target) {
                result.add(new ArrayList<>(list));
            }
            return;
        }
        
        // 递归左子树
        if (node.left != null) {
            Integer value = node.left.val;
            list.add(value);
            rec(node.left, list, sum+value, target);
            list.remove(value);
        }
        // 递归右子树
        if (node.right != null) {
            Integer value = node.right.val;
            list.add(value);
            rec(node.right, list, sum+value, target);
            list.remove(value);
        }
    }
}
```

### 25. 复杂链表的复制

#### 题目描述

> 输入一个复杂链表（每个节点中有节点值，以及两个指针，一个指向下一个节点，另一个特殊指针指向任意一个节点），返回结果为复制后复杂链表的head。（注意，输出结果中请不要返回参数中的节点引用，否则判题程序会直接返回空）
> 
> 题目链接：[https://www.nowcoder.com/practice/f836b2c43afc4b35ad6adc41ec941dba](https://www.nowcoder.com/practice/f836b2c43afc4b35ad6adc41ec941dba)

#### 解题思路

> 1、复制每个节点，到源结点的 next 处；2、重新遍历链表，调整 cloneNode 的 random 指向；3、拆分链表，返回复制链表

```java
public class Solution {
    public RandomListNode Clone(RandomListNode pHead) {
        if (pHead == null) return pHead;
        
        RandomListNode curNode = pHead;
        
        // 1. 复制每个节点，到源结点的 next 处
        while (curNode != null) {
            RandomListNode cloneNode = new RandomListNode(curNode.label);
            RandomListNode nextNode = curNode.next;
            curNode.next = cloneNode;
            cloneNode.next = nextNode;
            curNode = nextNode;
        }
        
        // 2. 重新遍历链表，调整 cloneNode 的 random 指向
        curNode = pHead;
        while (curNode != null) {
            curNode.next.random = (curNode.random == null ? null : curNode.random.next);
            curNode = curNode.next.next;
        }
        
        // 3. 拆分链表
        curNode = pHead;
        RandomListNode cloned = pHead.next;
        while (curNode != null) {
            RandomListNode cloneNode = curNode.next;
            curNode.next = cloneNode.next;
            cloneNode.next = (cloneNode.next == null ? null : cloneNode.next.next);
            curNode = curNode.next;
        }
        return cloned;
    }
}
```

### 26. 二叉搜索树与双向链表

#### 题目描述

> 输入一棵二叉搜索树，将该二叉搜索树转换成一个排序的双向链表。要求不能创建任何新的结点，只能调整树中结点指针的指向
> 
> 题目链接：[https://www.nowcoder.com/practice/947f6eb80d944a84850b0538bf0ec3a5](https://www.nowcoder.com/practice/947f6eb80d944a84850b0538bf0ec3a5)

#### 解题思路

> 解法1：迭代（非递归）思路，模拟中序遍历，记录上一个遍历的节点，同当前节点进行双向指向  
> 解法2：递归法

```java
/**
 * 解法1：迭代（非递归）法
 */
import java.util.Stack;

public class Solution {
    public TreeNode Convert(TreeNode pRootOfTree) {
        if (pRootOfTree == null) return null;
        
        Stack<TreeNode> stack = new Stack<>();
        TreeNode root = null;
        TreeNode p = pRootOfTree;
        TreeNode pre = null;
        boolean isFirst = true;
        
        while (p != null || !stack.isEmpty()) {
            while (p != null) {
                stack.push(p);
                p = p.left;
            }
            p = stack.pop();
            if (isFirst) {
                root = p;
                pre = p;
                isFirst = false;
            } else {
                pre.right = p;
                p.left = pre;
                pre = p;
            }
            p = p.right;
        }
        return root;
    }
}
```

### 27. 字符串的排列

#### 题目描述

> 输入一个字符串,按字典序打印出该字符串中字符的所有排列。例如输入字符串 abc，则打印出由字符 a,b,c 所能排列出来的所有字符串 abc,acb,bac,bca,cab和cba
> f
> 题目链接：[https://www.nowcoder.com/practice/fe6b651b66ae47d7acce78ffdd9a96c7](https://www.nowcoder.com/practice/fe6b651b66ae47d7acce78ffdd9a96c7)

#### 解题思路

> 1. 递归法（回溯）
> 2. 迭代法（字典生成）[后续更新]

```java
import java.util.ArrayList;
import java.util.Collections;

public class Solution {
    public ArrayList<String> Permutation(String str) {
        ArrayList<String> result = new ArrayList<>();
        rec(str.toCharArray(), 0, result);
        Collections.sort(result);
        return result;
    }
    
    private void rec(char[] chr, int i, ArrayList<String> result) {
        if (i == chr.length - 1) {
            String value = String.valueOf(chr);
            if (!result.contains(value)) {
                result.add(value);
            }
        } else {
            for (int j = i; j < chr.length; j++) {
                swap(i, j, chr);
                rec(chr, i+1, result);
                swap(i, j, chr);
            }
        }
    }
    
    private void swap(int i, int j, char[] chr) {
        char tmp = chr[i];
        chr[i] = chr[j];
        chr[j] = tmp;
    }
}
```

### 28. 数组中出现次数超过一半的数字

#### 题目描述

> 数组中有一个数字出现的次数超过数组长度的一半，请找出这个数字。例如输入一个长度为9的数组{1,2,3,2,2,2,5,4,2}。由于数字2在数组中出现了5次，超过数组长度的一半，因此输出2。如果不存在则输出0
> 
> 题目链接：[https://www.nowcoder.com/practice/e8a1b01a2df14cb2b228b30ee6a92163](https://www.nowcoder.com/practice/e8a1b01a2df14cb2b228b30ee6a92163)

#### 解题思路

> 利用 map 记录每个数字出现的次数，并且记录当前最大次数的数字

```java
import java.util.Map;
import java.util.HashMap;

public class Solution {
    public int MoreThanHalfNum_Solution(int [] array) {
        Map<Integer, Integer> map = new HashMap<>();
        int max = -1;
        int res = 0;
        for (int i = 0; i < array.length; i++) {
            int value = map.getOrDefault(array[i], 0) + 1;
            if (value > max) {
                max = value;
                res = array[i];
            }
            map.put(array[i], value);
        }
        return max > array.length / 2 ? res : 0;
    }
}
```

### 29. 最小的k个数

#### 题目描述

> 输入n个整数，找出其中最小的K个数。例如输入4,5,1,6,2,7,3,8这8个数字，则最小的4个数字是1,2,3,4
> 
> 题目链接：[https://www.nowcoder.com/practice/6a296eb82cf844ca8539b57c23e6e9bf](https://www.nowcoder.com/practice/6a296eb82cf844ca8539b57c23e6e9bf)

#### 解题思路

> 快排 partition 思想
> 大根堆思想

``` java
import java.util.*;

public class Solution {
    // 快排 partition 思想
    public ArrayList<Integer> GetLeastNumbers_Solution(int [] input, int k) {
        ArrayList<Integer> list = new ArrayList<>();
        if(input == null || input.length == 0 || k <= 0 || k > input.length){
             return list;
         }
        int start = 0;
        int end = input.length-1;
        
        int index = partition(input, start, end);
         while(index != k-1){
             if(index > k-1){
                 end = index - 1;
                 index = partition(input, start, end);
             }
             else{
                 start = index + 1;
                 index = partition(input, start, end);
             }
         }
        
        for (int i = 0; i < k; i++) {
            list.add(input[i]);
        }
        return list;
    }
    
    private int partition(int[] arr, int left, int right) {
        if(arr == null || arr.length == 0 || left < 0 || right >= arr.length){
             return -1;
         }
        int pivot = arr[left];
        while (left < right) {
            while (arr[right] >= pivot && left < right) right--;
            swap(arr, left, right);
            while (arr[left] <= pivot && left < right) left++;
            swap(arr, left, right);
        }
        return left;
    }
    
    private void swap(int[] arr, int m, int n) {
        int temp = arr[m];
        arr[m] = arr[n];
        arr[n] = temp;
    }
}
```

``` java
import java.util.*;

public class Solution {
    // 大根堆思想
    public ArrayList<Integer> GetLeastNumbers_Solution(int [] input, int k) {
        ArrayList<Integer> list = new ArrayList<>();
        if(input == null || input.length == 0 || k <= 0 || k > input.length){
             return list;
        }
        int[] kArray = Arrays.copyOfRange(input, 0, k);
        // 创建大根堆
        buildHeap(kArray);
        
        for (int i = k; i < input.length; i++) {
            if (input[i] < kArray[0]) {
                kArray[0] = input[i];
                maxHeap(kArray, 0);
            }
        }
        
        for (int i = 0; i < k; i++) {
            list.add(kArray[i]);
        }
        return list;
    }
    
    private void buildHeap(int[] input) {
        for (int i = input.length / 2 - 1; i >= 0; i--) {
            maxHeap(input, i);
        }
    }
    
    private void maxHeap(int[] input, int i) {
        int left = 2 * i + 1;
        int right = left + 1;
        int max = i;
        if (left < input.length && input[left] > input[max]) {
            max = left;
        }
        if (right < input.length && input[right] > input[max]) {
            max = right;
        }
        if (max != i) {
            swap(input, i, max);
            maxHeap(input, max);
        }
    }
    
    private void swap(int[] input, int i, int j) {
        int temp = input[i];
        input[i] = input[j];
        input[j] = temp;
    }
    
}
```

### 30. 连续子数组的最大和

#### 题目描述

> HZ 偶尔会拿些专业问题来忽悠那些非计算机专业的同学。今天测试组开完会后,他又发话了:在古老的一维模式识别中,常常需要计算连续子向量的最大和,当向量全为正数的时候,问题很好解决。  
> 但是,如果向量中包含负数,是否应该包含某个负数,并期望旁边的正数会弥补它呢？  
> 例如：{6,-3,-2,7,-15,1,2,2},连续子向量的最大和为8(从第0个开始,到第3个为止)。  
> 给一个数组，返回它的最大连续子序列的和，你会不会被他忽悠住？(子向量的长度至少是1)
> 
> 题目链接：[https://www.nowcoder.com/practice/459bd355da1549fa8a49e350bf3df484](https://www.nowcoder.com/practice/459bd355da1549fa8a49e350bf3df484)

#### 解题思路

> dp[i] = max(a[i], dp[i-1] + a[i])

```java
public class Solution {
    public int FindGreatestSumOfSubArray(int[] array) {
        int len = array.length;
        int[] dp = new int[len];
        dp[0] = array[0];
        int max = dp[0];
        for (int i = 1; i < array.length; i++) {
            dp[i] = Math.max(dp[i-1] + array[i], array[i]);
            max = Math.max(max, dp[i]);
        }
        return max;
    }
}
```

### 31. 整数中1出现的次数（从1到n整数中1出现的次数）

#### 题目描述

> 求出1~13的整数中1出现的次数，并算出100~1300的整数中1出现的次数？  
> 为此他特别数了一下1~13中包含1的数字有1、10、11、12、13因此共出现6次,但是对于后面问题他就没辙了。  
> ACMer希望你们帮帮他,并把问题更加普遍化,可以很快的求出任意非负整数区间中1出现的次数（从1 到 n 中1出现的次数）。
> 
> 题目链接：[https://www.nowcoder.com/practice/bd7f978302044eee894445e244c7eee6](https://www.nowcoder.com/practice/bd7f978302044eee894445e244c7eee6)

#### 解题思路

```java
public class Solution {
    public int NumberOf1Between1AndN_Solution(int n) {
        int count = 0;
        for (long i = 1; i <= n; i *= 10) {
            long driver = i * 10;
            count += (n / driver) * i + Math.min(Math.max(n % driver - i + 1, 0), i);
        }
        return count;
    }
}
```

### 32. 把数组排成最小的数

#### 题目描述

> 输入一个正整数数组，把数组里所有数字拼接起来排成一个数，打印能拼接出的所有数字中最小的一个。  
> 例如输入数组{3，32，321}，则打印出这三个数字能排成的最小数字为321323。
> 
> 题目链接：[https://www.nowcoder.com/practice/8fecd3f8ba334add803bf2a06af1b993](https://www.nowcoder.com/practice/8fecd3f8ba334add803bf2a06af1b993)

#### 解题思路

```java
import java.util.List;
import java.util.ArrayList;
import java.util.Collections;
import java.util.Comparator;

public class Solution {
    public String PrintMinNumber(int [] numbers) {
        List<Integer> list = new ArrayList<>();
		for (int num : numbers) {
			list.add(num);
		}
		Collections.sort(list, new Comparator<Integer>() {

			@Override
			public int compare(Integer o1, Integer o2) {
				// TODO Auto-generated method stub
				String a = o1 + "" + o2;
				String b = o2 + "" + o1;
				return a.compareTo(b);
			}
			
		});
		String string = "";
		for (Integer integer : list) {
			string += integer;
		}
		return string;
    }
}
```

### 33. 丑数

#### 题目描述

> 把只包含质因子2、3和5的数称作丑数（Ugly Number）。例如6、8都是丑数，但14不是，因为它包含质因子7。习惯上我们把1当做是第一个丑数。求按从小到大的顺序的第N个丑数
> 
> 题目链接：[https://www.nowcoder.com/practice/6aa9e04fc3794f68acf8778237ba065b](https://www.nowcoder.com/practice/6aa9e04fc3794f68acf8778237ba065b)

#### 解题思路

> 丑数 p = 2 ^ x + 3 ^ y + 5 ^ z，简而言之，丑数是上一个丑数乘以2或3或5得到的

```java
public class Solution {
    public int GetUglyNumber_Solution(int index) {
        if (index <= 0) return 0;
        List<Integer> list = new ArrayList<>();
        list.add(1);
        int idx_2 = 0, idx_3 = 0, idx_5 = 0;
        while (list.size() < index) {
            int m2 = list.get(idx_2) * 2;
            int m3 = list.get(idx_3) * 3;
            int m5 = list.get(idx_5) * 5;
            int min = Math.min(m2, Math.min(m3, m5));
            list.add(min);
            if (min == m2) idx_2++;
            if (min == m3) idx_3++;
            if (min == m5) idx_5++;
        }
        return list.get(index - 1);
    }
}
```

### 34. 第一个只出现一次的字符位置

#### 題目描述

> 在一个字符串(0<=字符串长度<=10000，全部由字母组成)中找到第一个只出现一次的字符,并返回它的位置, 如果没有则返回 -1（需要区分大小写）
> 
> 題目连接：[https://www.nowcoder.com/practice/1c82e8cf713b4bbeb2a5b31cf5b0417c](https://www.nowcoder.com/practice/1c82e8cf713b4bbeb2a5b31cf5b0417c)

#### 解题思路

> 利用 hashmap 或者 数组记录每个字符出现的次数，时间复杂度为：O（2*N）

```java
// 此处选用 数组
public class Solution {
    public int FirstNotRepeatingChar(String str) {
        char[] chr = str.toCharArray();
        int[] arr = new int['z' + 1];
        for (char c : chr) {
            arr[(int) c] += 1;
        }
        for (int i = 0; i < chr.length; i++) {
            if (arr[(int) chr[i]] == 1) {
                return i;
            }
        }
        return -1;
    }
}
```

### 35. 数组中的逆序对

#### 题目描述

> 在数组中的两个数字，如果前面一个数字大于后面的数字，则这两个数字组成一个逆序对。输入一个数组,求出这个数组中的逆序对的总数P。并将P对1000000007取模的结果输出。 即输出P%1000000007
> 
> 题目链接：[https://www.nowcoder.com/practice/96bd6684e04a44eb80e6a68efc0ec6c5](https://www.nowcoder.com/practice/96bd6684e04a44eb80e6a68efc0ec6c5)

#### 解题思路

> 利用归并排序的特性，得到当前序列段中，大于该元素的个数

```java
public class Solution {
    int res;
    int mod = 1000000007;
    public int InversePairs(int [] array) {
        res = 0;
        MergeSort(array, 0, array.length-1);
        return res;
    }
    
    private void MergeSort(int[] array, int low, int high) {
        if (low < high) {
            int mid = (low + high) >> 1;
            MergeSort(array, low, mid);
            MergeSort(array, mid+1, high);
            Merge(array, low, high);
        }
    }
    
    private void Merge(int[] array, int low, int high) {
        int[] temp = new int[high - low + 1];
        int mid = (low + high) >> 1;
        int i = low, j = mid + 1, k = 0;
        while (i <= mid && j <= high) {
            if (array[i] <= array[j]) {
                temp[k++] = array[i++];
            } else {
                temp[k++] = array[j++];
                res = res + (mid - i + 1);
                res %= mod;
            }
        }
        while (i <= mid) {
            temp[k++] = array[i++];
        }
        while (j <= high) {
            temp[k++] = array[j++];
        }
        for (k = 0; k < temp.length; k++) {
            array[k + low] = temp[k];
        }
    }
}
```

### 36. 两个链表的第一个公共结点

#### 题目描述

> 输入两个链表，找出它们的第一个公共结点
> 
> 题目链接：[https://www.nowcoder.com/practice/6ab1d9a29e88450685099d45c9e31e46](https://www.nowcoder.com/practice/6ab1d9a29e88450685099d45c9e31e46)

#### 解题思路

> 链表的公共结点开始的后面一部分一定是想等的，根据这个特点，我们作如下操作：  
> 首先假设长链表长度为 m，短链表为 n，去除长链表的前（m-n）个元素，然后我们开始一起遍历两个两个链表，直到找到相同结点

```java
public class Solution {
    public ListNode FindFirstCommonNode(ListNode pHead1, ListNode pHead2) {
        ListNode p1 = pHead1;
        ListNode p2 = pHead2;
        int len1 = findListLength(pHead1);
        int len2 = findListLength(pHead2);
        if (len1 < len2) {
            pHead2 = walkExtra(pHead2, len2-len1);
        } else if (len1 > len2) {
            pHead1 = walkExtra(pHead1, len1-len2);
        }
        while (pHead1 != pHead2) {
        	pHead1 = pHead1.next;
        	pHead2 = pHead2.next;
        }
        return pHead1;
    }

    private int findListLength(ListNode pHead) {
        int len = 0;
        while (pHead != null) {
            len++;
            pHead = pHead.next;
        }
        return len;
    }

    private ListNode walkExtra(ListNode pHead, int len) {
        for (int i = 0; i < len; i++) {
            pHead = pHead.next;
        }
        return pHead;
    }
}
```

### 37. 数字在排序数组中出现的次数

#### 题目描述

> 统计一个数字在排序数组中出现的次数
> 
> 题目链接：[https://www.nowcoder.com/practice/70610bf967994b22bb1c26f9ae901fa2](https://www.nowcoder.com/practice/70610bf967994b22bb1c26f9ae901fa2)

#### 解题思路

> 可以参考 [leetcode34：在排序数组中查找元素的第一个和最后一个位置](https://leetcode-cn.com/problems/find-first-and-last-position-of-element-in-sorted-array/description/)

```java
public class Solution {
    public int GetNumberOfK(int[] array , int k) {
        int left = findLeft(array, k);
        int right = findRight(array, k);
        return left == -1 ? 0 : (right - left + 1);
    }

    private int findLeft(int[] nums, int target) {
        int low = 0;
        int high = nums.length - 1;
        int mid = 0, idx = -1;

        while (low <= high) {
            mid = (low + high) >> 1;
            if (nums[mid] < target) {
                low = mid + 1;
            } else if (nums[mid] > target) {
                high = mid - 1;
            } else {
                // 记录下标
                idx = mid;
                // 左边界，往左继续寻找
                high = mid - 1;
            }
        }
        return idx;

    }

    private int findRight(int[] nums, int target) {
        int low = 0;
        int high = nums.length - 1;
        int mid = 0, idx = -1;

        while (low <= high) {
            mid = (low + high) >> 1;
            if (nums[mid] < target) {
                low = mid + 1;
            } else if (nums[mid] > target) {
                high = mid - 1;
            } else {
                // 记录下标
                idx = mid;
                // 右边界，往右继续寻找
                low = mid + 1;
            }
        }
        return idx;
    }
}
```

### 38. 二叉树的深度

#### 题目描述

> 输入一棵二叉树，求该树的深度。从根结点到叶结点依次经过的结点（含根、叶结点）形成树的一条路径，最长路径的长度为树的深度
> 
> 题目链接：[https://www.nowcoder.com/practice/435fb86331474282a3499955f0a41e8b](https://www.nowcoder.com/practice/435fb86331474282a3499955f0a41e8b)

```java
public class Solution {
    public int TreeDepth(TreeNode root) {
        if (root == null) return 0;
        int depthL = TreeDepth(root.left);
        int depthR = TreeDepth(root.right);
        return Math.max(depthL, depthR) + 1;
    }
}
```

### 39. 平衡二叉树

#### 题目描述

> 输入一棵二叉树，判断该二叉树是否是平衡二叉树
> 
> 题目链接：[https://www.nowcoder.com/practice/8b3b95850edb4115918ecebdf1b4d222](https://www.nowcoder.com/practice/8b3b95850edb4115918ecebdf1b4d222)

```java
public class Solution {
    public boolean IsBalanced_Solution(TreeNode root) {
        if (root == null) return true;
        int left = find_depth(root.left, 0);
        int right = find_depth(root.right, 0);
        if (Math.abs(right - left) <= 1) {
            return IsBalanced_Solution(root.left) && IsBalanced_Solution(root.right);
        }
        return false;
    }
    
    public int find_depth(TreeNode root, int depth) {
        if (root == null) return depth;
        return Math.max(find_depth(root.left, depth+1), find_depth(root.right, depth+1));
    }
}
```

### 40. 数组中只出现一次的数字

#### 题目描述

> 一个整型数组里除了两个数字之外，其他的数字都出现了偶数次。请写程序找出这两个只出现一次的数字
> 
> 题目链接：[https://www.nowcoder.com/practice/e02fdb54d7524710a7d664d082bb7811](https://www.nowcoder.com/practice/e02fdb54d7524710a7d664d082bb7811)

#### 解题思路

> 我们可以先考虑一个简单的问题：一个数组里除了一个数字以外，其他的都出现了两次，请找出这个数字  
> 我们知道 a ^ a = 0，所以如果将数组里所有元素进行异或运算，得到的结果会是只出现了一次的数字  
> 那么回到这道题，有两个数字出现了一次，那个我们希望把这个数组拆分成两个小数组，就可以通过上述做法得到结果值。假设结果为 a 和 b，我们可以知道的是，该数组中的所有元素的异或结果 = a ^ b，而且 a 和 b 的异或的二进制结果必然有一个 1（假设在位置 idx处），那么我们根据元素是否在 idx 处为 1，进行划分，便可得到两个小数组

```java
//num1,num2分别为长度为1的数组。传出参数
//将num1[0],num2[0]设置为返回结果
public class Solution {
    public void FindNumsAppearOnce(int [] array,int num1[] , int num2[]) {
        if (array == null || array.length < 2) {
            return;
        }
        int bit = 0;
        for (int i : array) {
            bit ^= i;
        }
        int idx = findFirst(bit);
        for (int i : array) {
            if (isBit(i, idx)) {
                num1[0] ^= i;
            } else {
                num2[0] ^= i;
            }
        }
    }
    
    private int findFirst(int num) {
        int idx = 0;
        while ((num & 1) == 0) {
            num >>= 1;
            idx++;
        }
        return idx;
    }
    
    private boolean isBit(int num, int idx) {
        num >>= idx;
        return (num & 1) == 1;
    }
}
```

### 41. 和为S的连续正数序列

#### 题目描述

> 小明很喜欢数学,有一天他在做数学作业时,要求计算出9~16的和,他马上就写出了正确答案是100。  
> 但是他并不满足于此,他在想究竟有多少种连续的正数序列的和为100(至少包括两个数)。  
> 没多久,他就得到另一组连续正数和为100的序列:18,19,20,21,22。现在把问题交给你,你能不能也很快的找出所有和为S的连续正数序列? 
> 
> 题目链接：[https://www.nowcoder.com/practice/c451a3fd84b64cb19485dad758a55ebe](https://www.nowcoder.com/practice/c451a3fd84b64cb19485dad758a55ebe)

#### 解题思路

> 解法1：利用等差数列求和公式，暴力得到右边界的可能值 

```java
public class Solution {
    public ArrayList<ArrayList<Integer> > FindContinuousSequence(int sum) {
        ArrayList<ArrayList<Integer>> result = new ArrayList<>();
        for (int i = 1; i <= sum / 2; i++) {
        	int temp = sum * 2 + i * i - i;
            int j = (int) Math.sqrt(temp);
            if ((j - 1) * j == temp) {
                result.add(generator(i, j - 1));
            } else if ((j + 1) * j == temp) {
            	result.add(generator(i, j));
            }
        }
        return result;
    }
    
    private ArrayList<Integer> generator(int left, int right) {
        ArrayList<Integer> list = new ArrayList<>();
        for (int i = left; i <= right; i++) {
            list.add(i);
        }
        return list;
    }
}
```

### 42. 和为S的两个数字

#### 题目描述

> 输入一个递增排序的数组和一个数字S，在数组中查找两个数，使得他们的和正好是S，如果有多对数字的和等于S，输出两个数的乘积最小的
> 
> 题目链接：[https://www.nowcoder.com/practice/390da4f7a00f44bea7c2f3d19491311b](https://www.nowcoder.com/practice/390da4f7a00f44bea7c2f3d19491311b)


```java
public class Solution {
    public ArrayList<Integer> FindNumbersWithSum(int [] array,int sum) {
        int left = 0;
        int right = array.length - 1;
        int multiply = Integer.MAX_VALUE;
        int i = -1;
        int j = -1;
        while (left < right) {
        	int target = array[left] + array[right];
        	if (target < sum) {
				left ++;
			} else if (target > sum) {
				right --;
			} else {
				if (array[left] * array[right] < multiply) {
					i = left;
					j = right;
                    multiply = array[left] * array[right];
				}
				left ++;
				right --;
			}
        }
        if (i == -1) {
			return new ArrayList<>();
		}
        List<Integer> result = Arrays.asList(array[i], array[j]);
        return new ArrayList<>(result);
    }
}
```

### 43. 左旋转字符串

#### 题目描述

> 汇编语言中有一种移位指令叫做循环左移（ROL），现在有个简单的任务，就是用字符串模拟这个指令的运算结果  
> 对于一个给定的字符序列S，请你把其循环左移K位后的序列输出  
> 例如，字符序列S=”abcXYZdef”,要求输出循环左移3位后的结果，即“XYZdefabc”。是不是很简单？OK，搞定它！
> 
> 题目链接：[https://www.nowcoder.com/practice/12d959b108cb42b1ab72cef4d36af5ec](https://www.nowcoder.com/practice/12d959b108cb42b1ab72cef4d36af5ec)

#### 解题思路

> 解法：YX = (X<sup>T</sup>Y<sup>T</sup>)<sup>T</sup>

```java
public class Solution {
    public String LeftRotateString(String str,int n) {
        int len = str.length();
        if (len < n) {
			return str;
		}
        char[] chars = str.toCharArray();
        reverse(chars, 0, n-1);
        reverse(chars, n, len-1);
        reverse(chars, 0, len-1);
        return String.valueOf(chars);
    }
	
	private void reverse(char [] chars, int low, int high) {
		char temp;
		while (low < high) {
			temp = chars[low];
			chars[low++] = chars[high];
			chars[high--] = temp;
		}
	}
}
```

### 44. 翻转单词顺序列

#### 题目描述

> 牛客最近来了一个新员工Fish，每天早晨总是会拿着一本英文杂志，写些句子在本子上，同事Cat对Fish写的内容颇感兴趣，有一天他向Fish借来翻看，但却读不懂它的意思  
> 例如，“student. a am I”。后来才意识到，这家伙原来把句子单词的顺序翻转了，正确的句子应该是“I am a student.”。Cat对一一的翻转这些单词顺序可不在行，你能帮助他么？
> 
> 题目链接：[https://www.nowcoder.com/practice/3194a4f4cf814f63919d0790578d51f3](https://www.nowcoder.com/practice/3194a4f4cf814f63919d0790578d51f3)

#### 解题思路

> 解法：先翻转整个句子，然后，依次翻转每个单词

```java
public class Solution {
    public String ReverseSentence(String str) {
		if (str == null || "".equals(str)) {
			return "";
		}
		int len = str.length();
		char[] chars = str.toCharArray();
		reverse(chars, 0, len-1);
		int left = 0;
		for (int i = 0; i < len; i++) {
			if (chars[i] == ' ') {
				reverse(chars, left, i-1);
				left = i+1;
			}
		}
        reverse(chars, left, len-1);
		return String.valueOf(chars);
	}
	
	private void reverse(char [] chars, int low, int high) {
		char temp;
		while (low < high) {
			temp = chars[low];
			chars[low++] = chars[high];
			chars[high--] = temp;
		}
	}
}
```