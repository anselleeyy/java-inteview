# 剑指 Offer

## 目录

- [1 二维数组中的查找](#1-二维数组中的查找)
- [2 替换空格](#2-替换空格)
- [3 从尾到头打印链表](#3-从尾到头打印链表)
- [4 重建二叉树](#4-重建二叉树)
- [5 用两个栈实现队列](#5-用两个栈实现队列)
- [6 旋转数组的最小数字](#6-旋转数组的最小数字)
- [7 斐波那契数列](#7-斐波那契数列)
- [8 跳台阶](#8-跳台阶)
- [9 变态跳台阶](#9-变态跳台阶)
- [10 矩阵覆盖](#10-矩阵覆盖)
- [11 二进制中1的个数](#11-二进制中1的个数)
- [12 数值的整数次方](#12-数值的整数次方)
- [13 调整数组顺序使奇数位于偶数前面](#13-调整数组顺序使奇数位于偶数前面)
- [14 链表中倒数第k个结点](#14-链表中倒数第k个结点)
- [15 反转链表](#15-反转链表)
- [16 合并两个排序链表](#16-合并两个排序链表)
- [17 树的子结构](#17-树的子结构)
- [18 二叉树的镜像](#18-二叉树的镜像)
- [19 顺时针打印矩阵](#19-顺时针打印矩阵)
- [20 包含min函数的栈](#20-包含min函数的栈)
- [21 栈的压入、弹出序列](#21-栈的压入、弹出序列)
- [22 从上往下打印二叉树](#22-从上往下打印二叉树)
- [23 二叉搜索树的后序遍历序列](#23-二叉搜索树的后序遍历序列)
- [24 二叉树中和为某一值的路径](#24-二叉树中和为某一值的路径)
- [25 复杂链表的复制](#25-复杂链表的复制)
- [26 二叉搜索树与双向链表](#26-二叉搜索树与双向链表)
- [27 字符串的排列](#27-字符串的排列)
- [28 数组中出现次数超过一半的数字](#28-数组中出现次数超过一半的数字)
- [29 最小的 k 个数](#29-最小的k个数)
- [30 连续子数组的最大和](#30-连续子数组的最大和)
- [31 整数中1出现的次数（从1到n整数中1出现的次数）](#31-整数中1出现的次数（从1到n整数中1出现的次数）)
- [32 把数组排成最小的数](#32-把数组排成最小的数)
- [33 丑数](#33-丑数)
- [34 第一个只出现一次的字符位置](#34-第一个只出现一次的字符位置)
- [35 数组中的逆序对](#35-数组中的逆序对)
- [36 两个链表的第一个公共结点](#36-两个链表的第一个公共结点)
- [37 数字在排序数组中出现的次数](#37-数字在排序数组中出现的次数)
- [38 二叉树的深度](#38-二叉树的深度)
- [39 平衡二叉树](#39-平衡二叉树)
- [40 数组中只出现一次的数字](#40-数组中只出现一次的数字)
- [41 和为S的连续正数序列](#41-和为S的连续正数序列)
- [42 和为S的两个数字](#42-和为S的两个数字)
- [43 左旋转字符串](#43-左旋转字符串)
- [44 翻转单词顺序列](#44-翻转单词顺序列)
- [45 扑克牌顺子](#45-扑克牌顺子)
- [46 孩子们的游戏(圆圈中最后剩下的数)](#46-孩子们的游戏圆圈中最后剩下的数)
- [47 求1+2+3+...+n](#47-求123n)
- [48 不用加减乘除做加法](#48-不用加减乘除做加法)
- [49 把字符串转换成整数](#49-把字符串转换成整数)
- [50 数组中重复的数字](#50-数组中重复的数字)
- [51 构建乘积数组](#51-构建乘积数组)
- [52 正则表达式匹配](#52-正则表达式匹配)
- [53 表示数值的字符串](#53-表示数值的字符串)
- [54 字符流中第一个不重复的字符](#54-字符流中第一个不重复的字符)
- [55 链表中环的入口结点](#55-链表中环的入口结点)
- [56 删除链表中重复的结点](#56-删除链表中重复的结点)
- [57 二叉树的下一个结点](#57-二叉树的下一个结点)
- [58 对称的二叉树](#58-对称的二叉树)
- [59 按之字形顺序打印二叉树](#59-按之字形顺序打印二叉树)
- [60 把二叉树打印成多行](#60-把二叉树打印成多行)
- [61 序列化二叉树](#61-序列化二叉树)
- [62 二叉搜索树的第k个结点](#62-二叉搜索树的第k个结点)
- [63 数据流中的中位数](#63-数据流中的中位数)
- [64 滑动窗口的最大值](#64-滑动窗口的最大值)
- [65 矩阵中的路径](#65-矩阵中的路径)
- [66 机器人的运动范围](#66-机器人的运动范围)

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
        if (input == null || input.length == 0 || k <= 0 || k > input.length) {
            return list;
        }
        int start = 0;
        int end = input.length-1;
        
        int index = partition(input, start, end);
        while (index != k-1) {
            if (index > k-1) {
                end = index - 1;
                index = partition(input, start, end);
            }
            else {
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

### 45. 扑克牌顺子

#### 题目描述

> LL今天心情特别好，因为他去买了一副扑克牌，发现里面居然有2个大王，2个小王(一副牌原本是54张^_^)...  
> 他随机从中抽出了5张牌，想测测自己的手气，看看能不能抽到顺子，如果抽到的话，他决定去买体育彩票，嘿嘿！！  
> “红心A，黑桃3，小王，大王，方片5”，“Oh My God!” 不是顺子.....LL不高兴了，他想了想，决定大、小王可以看成任何数字，并且A看作1，J为11，Q为12，K为13  
> 上面的5张牌就可以变成“1,2,3,4,5”(大小王分别看作2和4),“So Lucky!”。LL决定去买体育彩票啦  
> 现在，要求你使用这幅牌模拟上面的过程，然后告诉我们LL的运气如何， 如果牌能组成顺子就输出true，否则就输出false。为了方便起见,你可以认为大小王是0。
> 
> 题目链接：[https://www.nowcoder.com/practice/762836f4d43d43ca9deb273b3de8e1f4](https://www.nowcoder.com/practice/762836f4d43d43ca9deb273b3de8e1f4)

#### 解题思路

> 解法1：
>   1. 排序
>   2. 计算所有相邻数字间隔总数
>   3. 计算 0 的个数
>   4. 如果2、3相等，就是顺子
>   5. 如果出现对子，则不是顺子

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

> 解法2：
>   1. max - min < 5
>   2. 除0外没有重复的数字

``` java
public class Solution {
    public boolean isContinuous(int [] numbers) {
        int zero_num = 0;
        int len = numbers.length - 1;
        if (len == -1) {
            return false;
        }
        int min = Integer.MAX_VALUE;
        int max = Integer.MIN_VALUE;
        int [] diff = new int[14];
        for (int i = 0; i < len; i++) {
            diff[numbers[i]]++;
            if (numbers[i] == 0) {
                zero_num++;
                continue;
            }
            if (diff[numbers[i]] > 1) {
                return false;
            }
            max = Math.max(numbers[i], max);
            min = Math.min(numbers[i], min);
        }
        if (max - min >= 5) {
            return false;
        }
        return true;
    }
}
```

### 46. 孩子们的游戏(圆圈中最后剩下的数)

#### 题目描述

> 每年六一儿童节，牛客都会准备一些小礼物去看望孤儿院的小朋友，今年亦是如此。HF作为牛客的资深元老，自然也准备了一些小游戏  
> 其中，有个游戏是这样的：首先，让小朋友们围成一个大圈。然后，他随机指定一个数m，让编号为0的小朋友开始报数。每次喊到m-1的那个小朋友要出列唱首歌，然后可以在礼品箱中任意的挑选礼物，并且不再回到圈中，从他的下一个小朋友开始，继续0...m-1报数  
> 这样下去，直到剩下最后一个小朋友，可以不用表演，并且拿到牛客名贵的“名侦探柯南”典藏版(名额有限哦!!^_^)。请你试着想下，哪个小朋友会得到这份礼品呢？(注：小朋友的编号是从0到n-1)
> 
> 题目链接：[https://www.nowcoder.com/practice/f78a359491e64a50bce2d89cff857eb6](https://www.nowcoder.com/practice/f78a359491e64a50bce2d89cff857eb6)

#### 解题思路

> 1. 约瑟夫环公式解法
> 2. 模拟
> 3. 利用 LinkedList 简化模拟

``` java
/* 解法1：约瑟夫环公式 */
public class Solution {
    public int LastRemaining_Solution(int n, int m) {
        if (n == 0) {
            return -1;
        } else if (n == 1) {
            return 0;
        } else {
            return (LastRemaining_Solution(n-1, m) + m) % n;
        }
    }
}

/* 解法2：模拟 */
public class Solution {
    public int LastRemaining_Solution(int n, int m) {
        if (n < 1 || m < 1) return -1;
        int[] arr = new int[n];
        int i = -1, step = 0, count = n;
        while (count > 0) {
            i++;
            if (i >= n) {
                i = 0;  // 模拟环
            }
            if (arr[i] == -1) {
                continue;  // 跳过删除的节点
            }
            step++;
            if (step == m) {
                arr[i] = -1;
                step = 0;
                count--;
            }
        }
        return i;
    }
}

/* 解法3：利用 LinkedList 简化模拟 */
public class Solution {
    public int LastRemaining_Solution(int n, int m) {
        LinkedList<Integer> list = new LinkedList<>();
        for (int i = 0; i < n; i++) {
            list.add(i);
        }
        int step = 0;
        while (list.size() > 1) {
            step = (step + m - 1) % list.size();
            list.remove(step);
        }
        return list.size() == 1 ? list.get(0) : -1;
    }
}
```

### 47. 求1+2+3+...+n

#### 题目描述

> 求1+2+3+...+n，要求不能使用乘除法、for、while、if、else、switch、case等关键字及条件判断语句（A ? B : C）  
> 
> 题目链接：[https://www.nowcoder.com/practice/7a0da8fc483247ff8800059e12d7caf1](https://www.nowcoder.com/practice/7a0da8fc483247ff8800059e12d7caf1)

#### 解题思路

> 需利用逻辑与的短路特性实现递归终止

``` java
public class Solution {
    public int Sum_Solution(int n) {
        int res = n;
        boolean t = (res > 0) && ((res += Sum_Solution(n - 1)) > 0);
        return res;
    }
}
```

### 48. 不用加减乘除做加法

#### 题目描述

> 写一个函数，求两个整数之和，要求在函数体内不得使用+、-、*、/四则运算符号。  
> 
> 题目链接：[https://www.nowcoder.com/practice/59ac416b4b944300b617d4f7f111b215](https://www.nowcoder.com/practice/59ac416b4b944300b617d4f7f111b215)

#### 解题思路

1. 两个数异或：相当于每一位相加，而不考虑进位
2. 两个数相与，并左移一位：相当于求得进位
3. 将上述两步的结果相加

``` java
public class Solution {
    public int Add(int num1,int num2) {
        if (num2 == 0) {
            return num1;
        }
        int sum = num1 ^ num2;
        int carry = (num1 & num2) << 1;
        return Add(sum, carry);
    }
}
```

### 49. 把字符串转换成整数

#### 题目描述

> 将一个字符串转换成一个整数(实现Integer.valueOf(string)的功能，但是string不符合数字要求时返回0)，要求不能使用字符串转换整数的库函数  
> 数值为0或者字符串不是一个合法的数值则返回0
> 
> 题目链接：[https://www.nowcoder.com/practice/1277c681251b4372bdef344468e4f26e](https://www.nowcoder.com/practice/1277c681251b4372bdef344468e4f26e)

#### 解题思路

> 传统方法遍历字符数组即可，注意溢出和非法符号的处理

``` java
public class Solution {
    public int StrToInt(String str) {
        if (str == null || "".equals(str.trim())) {
            return 0;
        }
		
        int symbol = 0;
        int left = 0;
		
        char[] chars = str.toCharArray();
        if (chars[left] == '+' || chars[left] == '-') {
            symbol = chars[left] == '+' ? 0 : 1;
            left++;
        }
        int result = 0;
        for (int i = left; i < chars.length; i++) {
            if (chars[i] > '9' || chars[i] < '0') {
                return 0;
            }
            if (result < 0) {
                return 0;
            }
            result = result * 10 + (int) (chars[i] - '0');
            System.out.println(result);
        }
        result = (int) Math.pow(-1, symbol) * result;
        return result;
    }
}
```

### 50. 数组中重复的数字

#### 题目描述

> 在一个长度为n的数组里的所有数字都在0到n-1的范围内  
> 数组中某些数字是重复的，但不知道有几个数字是重复的。也不知道每个数字重复几次。请找出数组中任意一个重复的数字  
> 例如，如果输入长度为7的数组{2,3,1,0,2,5,3}，那么对应的输出是第一个重复的数字2
> 
> 题目链接：[https://www.nowcoder.com/practice/623a5ac0ea5b4e5f95552655361ae0a8](https://www.nowcoder.com/practice/623a5ac0ea5b4e5f95552655361ae0a8)

#### 解题思路

1. 把当前序列当成是一个下标和下标对应值是相同的数组
2. 遍历数组，判断当前位的值和下标是否相等
   1. 若相等，则遍历下一位
   2. 若不等，则将当前位置i上的元素和a[i]位置上的元素比较
      1. 若它们相等，则成功
      2. 若不等，则将它们两交换
   3. 换完之后a[i]位置上的值和它的下标是对应的，但i位置上的元素和下标并不一定对应
   4. 重复2.2的操作，直到当前位置i的值也为i，将i向后移一位，再重复2

``` java
public class Solution {
    // Parameters:
    //    numbers:     an array of integers
    //    length:      the length of array numbers
    //    duplication: (Output) the duplicated number in the array number,length of duplication array is 1,so using duplication[0] = ? in implementation;
    //                  Here duplication like pointor in C/C++, duplication[0] equal *duplication in C/C++
    //    这里要特别注意~返回任意重复的一个，赋值duplication[0]
    //    Return value: true if the input is valid, and there are some duplications in the array number otherwise false
    public boolean duplicate(int array[], int length, int[] duplication) {
        if (array == null || array.length != length) {
            return false;
        }
        for (int i = 0; i < length; i++) {
            if (array[i] < 0 || array[i] >= length) {
                return false;
            }
            while (array[i] != i) {
                if (array[i] == array[array[i]]) {
                    duplication[0] = array[i];
                    System.out.println(duplication[0]);
                    return true;
            	}
                swap(array, i, array[i]);
            }
        }
        System.out.println(false);
        return false;
    }
	
    private void swap(int[] array, int i, int j) {
        int temp = array[i];
        array[i] = array[j];
        array[j] = temp;
    }
}
```

### 51. 构建乘积数组

#### 题目描述

> 给定一个数组A[0,1,...,n-1],请构建一个数组B[0,1,...,n-1],其中B中的元素B[i]=A[0]*A[1]*...*A[i-1]*A[i+1]*...*A[n-1]。不能使用除法
> 
> 题目链接：[https://www.nowcoder.com/practice/94a4d381a68b47b7a8bed86f2975db46](https://www.nowcoder.com/practice/94a4d381a68b47b7a8bed86f2975db46)

#### 解题思路

> 对于第一个for循环  
> 第一步：b[0] = 1  
> 第二步：b[1] = b[0] * a[0] = a[0]  
> 第三步：b[2] = b[1] * a[1] = a[0] * a[1] ...  
> 对于第二个for循环  
> 第一步：temp = 1  
> 第二步：b[4] = b[4] * temp; temp *= a[4]  
> 第三步：b[3] *= temp; temp *= a[3] ...  

``` java
public class Solution {
    public int[] multiply(int[] A) {
        int[] B = new int[A.length];
        B[0] = 1;
        for (int i = 1; i < A.length; i++) {
            B[i] = B[i-1] * A[i-1];
        }
        int temp = 1;
        for (int i = A.length-1; i >= 0; i--) {
            B[i] *= temp;
            temp *= A[i];
        }
        return B;
    }
}
```

### 52. 正则表达式匹配

#### 题目描述

> 请实现一个函数用来匹配包括'.'和'\*' 的正则表达式  
> 模式中的字符'.'表示任意一个字符，而'\*'表示它前面的字符可以出现任意次（包含0次）  
> 在本题中，匹配是指字符串的所有字符匹配整个模式。例如，字符串"aaa"与模式"a.a"和"ab\*ac\*a"匹配，但是与"aa.a"和"ab\*a"均不匹配
> 
> 题目链接：[https://www.nowcoder.com/practice/45327ae22b7b413ea21df13ee7d6429c](https://www.nowcoder.com/practice/45327ae22b7b413ea21df13ee7d6429c)

#### 解题思路

- 当模式中的第二个字符是 "\*" 时
  - 如果字符串第一个字符跟模式第一个字符不匹配，则模式后移 2 个字符
  - 如果字符串第一个字符跟模式第一个字符匹配，可以有 3 种匹配方式
    - 模式后移 2 字符，相当于 x* 被忽略
    - 字符串后移 1 字符，模式后移 2 字符
    - 字符串后移 1 字符，模式不变，即继续匹配字符下一位，因为 * 可以匹配多位
- 当模式中的第二个字符不是 "\*" 时
  - 如果字符串第一个字符和模式中的第一个字符相匹配，那么字符串和模式都后移一个字符，然后匹配剩余的
  - 如果字符串第一个字符和模式中的第一个字符相不匹配，直接返回 false

``` java
public boolean match(char[] str, char[] pattern) {
    if (str == null || pattern == null) {
        return false;
    }
    return match(str, 0, pattern, 0);
}

public boolean match(char[] str, int strIndex, char[] pattern, int patternIndex) {
    if (strIndex == str.length && patternIndex == pattern.length) {
        return true;
    }
    if (strIndex != str.length && patternIndex == pattern.length) {
        return false;
    }
    // 模式中的第二个字符是 "*"
    if (patternIndex + 1 < pattern.length && pattern[patternIndex + 1] == '*') {
        if ((strIndex != str.length && pattern[patternIndex] == str[strIndex]) 
            || (pattern[patternIndex] == '.' && strIndex != str.length)) {
            return match(str, strIndex, pattern, patternIndex + 2)
                || match(str, strIndex + 1, pattern, patternIndex + 2)
                || match(str, strIndex + 1, pattern, patternIndex);
        } else {
        	// 字符串第一个字符跟模式第一个字符不匹配, 则模式后移2个字符
            return match(str, strIndex, pattern, patternIndex + 2);
        }
    }
    // 模式中的第二个字符不是 "*"
    // 如果字符串第一个字符和模式中的第一个字符相匹配，那么字符串和模式都后移一个字符
    if (strIndex != str.length) {
        if (pattern[patternIndex] == str[strIndex] || pattern[patternIndex] == '.') {
            return match(str, strIndex + 1, pattern, patternIndex + 1);
        }
    }
    return false;
 }
```

### 53. 表示数值的字符串

#### 题目描述

> 请实现一个函数用来判断字符串是否表示数值（包括整数和小数）  
> 例如，字符串"+100","5e2","-123","3.1416"和"-1E-16"都表示数值，但是"12e","1a3.14","1.2.3","+-5"和"12e+4.3"都不是  
> 
> 题目链接：[https://www.nowcoder.com/practice/6f8c901d091949a5837e24bb82a731f2](https://www.nowcoder.com/practice/6f8c901d091949a5837e24bb82a731f2)

#### 解题思路

> 查找 e(E)、正负号、小数点出现的地方，进行如下判断
> 1. e后面一定要接数字且e不能出现两次
> 2. +- 号 第一次出现不是在头部的 或者 第二次出现的，必须紧跟在 e(E) 之后
> 3. e 后面不能接小数点，小数点不能出现两次
>   

``` java
public class Solution {
    public boolean isNumeric(char[] str) {
        boolean sign 	= false;
        boolean decimal = false;
        boolean hasE 	= false;
		
        for (int i = 0; i < str.length; i++) {
            if (str[i] == 'e' || str[i] == 'E') {
                if (i == str.length - 1 || hasE) {
                    return false;
                }
                hasE = true;
            } else if (str[i] == '+' || str[i] == '-') {
                if ((sign || (!sign && i > 0)) && str[i-1] != 'e' && str[i-1] != 'E') {
                    return false;
                }
                sign = true;
            } else if (str[i] == '.') {
                if (hasE || decimal) {
                    return false;
                }
                decimal = true;
            } else if (!Character.isDigit(str[i])) {
                return false;
            }
        }
        return true;
    }
}
```

### 54. 字符流中第一个不重复的字符

#### 题目描述

> 请实现一个函数用来找出字符流中第一个只出现一次的字符；如果当前字符流没有存在出现一次的字符，返回#字符  
> 例如，当从字符流中只读出前两个字符"go"时，第一个只出现一次的字符是"g"。当从该字符流中读出前六个字符“google"时，第一个只出现一次的字符是"l"
> 
> 题目链接：[https://www.nowcoder.com/practice/00de97733b8e4f97a3fb5c680ee10720](https://www.nowcoder.com/practice/00de97733b8e4f97a3fb5c680ee10720)

#### 解题思路

> 利用一个alpha数组进行存储字符是否出现过

``` java
import java.util.List;
import java.util.ArrayList;

public class Solution {
    
    private List<Character> list = new ArrayList<>();
    
    private int[] alpha = new int[256];
    
    //Insert one char from stringstream
    public void Insert(char ch)
    {
        if (alpha[ch] == 0) {
            list.add(ch);
            alpha[ch] = 1;
        } else {
            list.remove((Character) ch);
        }
    }

    //return the first appearence once char in current stringstream
    public char FirstAppearingOnce()
    {
        if (list.size() != 0) {
            return list.get(0);
        }
        return '#';
    }
}
```

### 55. 链表中环的入口结点

#### 题目描述

> 给一个链表，若其中包含环，请找出该链表的环的入口结点，否则，输出null  
> 
> 题目链接：[https://www.nowcoder.com/practice/253d2c59ec3e4bc68da16833f79a38e4](https://www.nowcoder.com/practice/253d2c59ec3e4bc68da16833f79a38e4)

#### 解题思路

> 利用两个指针(fast 和 slow), 如果没有环，那么 fast 和 slow 不会相遇此时返回 null；如果有环，那 fast 和 slow 肯定会再次相遇  
> 相遇的时候，fast 刚好比 slow 多走了一圈环的长度。通过画图我们可以得知 slow 距离环起点的距离和 pHead 距离起点的距离是一样的  
> 所以我们可以再次进行一次循环，找到这个起点

``` java
public class Solution {
    public ListNode EntryNodeOfLoop(ListNode pHead) {
        ListNode fast = pHead;
        ListNode slow = pHead;
        while (fast != null && fast.next != null) {
            fast = fast.next.next;
            slow = slow.next;
            if (fast == slow) {
                ListNode p = pHead;
                while (p != slow) {
                    p = p.next;
                    slow = slow.next;
                }
                return p;
            }
        }
        return null;
    }
}
```

### 56. 删除链表中重复的结点

#### 题目描述

> 在一个排序的链表中，存在重复的结点，请删除该链表中重复的结点，重复的结点不保留，返回链表头指针。 例如，链表1->2->3->3->4->4->5 处理后为 1->2->5  
> 
> 题目链接：[https://www.nowcoder.com/practice/fc533c45b73a41b0b44ccba763f866ef](https://www.nowcoder.com/practice/fc533c45b73a41b0b44ccba763f866ef)

```java
/**
 * 递归解法
 */
public class Solution {
    public ListNode deleteDuplication(ListNode pHead)
    {
        if (pHead == null || pHead.next == null) {
            return pHead;
        }
        if (pHead.val == pHead.next.val) {
            ListNode pNode = pHead.next;
            while (pNode != null && pNode.val == pHead.val) {
                pNode = pNode.next;
            }
            return deleteDuplication(pNode);
        } else {
            pHead.next = deleteDuplication(pHead.next);
            return pHead;
        }
    }
}

/**
 * 非递归解法
 */
public class Solution {
    public ListNode deleteDuplication(ListNode pHead)
    {
        ListNode first = new ListNode(0);
        first.next = pHead;
        ListNode p = pHead;
        ListNode last = first;
        
        while (p != null && p.next != null) {
            if (p.val == p.next.val) {
                int value = p.val;
                while (p != null && p.val == value) {
                    p = p.next;
                }
                last.next = p;
            } else {
                last = p;
                p = p.next;
            }
        }
        return first.next;
    }
}
```

### 57. 二叉树的下一个结点

#### 题目描述

> 给定一个二叉树和其中的一个结点，请找出中序遍历顺序的下一个结点并且返回。注意，树中的结点不仅包含左右子结点，同时包含指向父结点的指针  
> 
> 题目链接：[https://www.nowcoder.com/practice/9023a0c988684a53960365b889ceaf5e](https://www.nowcoder.com/practice/9023a0c988684a53960365b889ceaf5e)

#### 解题思路

> 注意题目中二叉树结构中的next指针是指向父节点的指针

```java
public class Solution {
    public TreeLinkNode GetNext(TreeLinkNode pNode)
    {
        if (pNode == null) {
        return null;
        }
        
        if (pNode.right != null) {
            pNode = pNode.right;
            while (pNode.left != null) {
                pNode = pNode.left;
            }
            return pNode;
        }
        
        while (pNode.next != null) {
            TreeLinkNode node = pNode.next;
            if (node.left == pNode) {
                return node;
            }
            pNode = node;
        }
        return null;
    }
}
```

### 58. 对称的二叉树

#### 题目描述

> 请实现一个函数，用来判断一颗二叉树是不是对称的。注意，如果一个二叉树同此二叉树的镜像是同样的，定义其为对称的
> 
> 题目链接：[https://www.nowcoder.com/practice/ff05d44dfdb04e1d83bdbdab320efbcb](https://www.nowcoder.com/practice/ff05d44dfdb04e1d83bdbdab320efbcb)

```java
public class Solution {
    boolean isSymmetrical(TreeNode pRoot)
    {
        if (pRoot == null) return true;
        return compare_root(pRoot.left, pRoot.right);
    }
    
    boolean compare_root(TreeNode left, TreeNode right) {
        if (left == null) return right == null;
        if (right == null) return false;
        if (left.val != right.val) return false;
        return compare_root(left.right, right.left) && compare_root(left.left, right.right);
    }
}
```

### 59. 按之字形顺序打印二叉树

#### 题目描述

> 请实现一个函数按照之字形打印二叉树，即第一行按照从左到右的顺序打印，第二层按照从右至左的顺序打印，第三行按照从左到右的顺序打印，其他行以此类推
> 
> 题目链接：[https://www.nowcoder.com/practice/91b69814117f4e8097390d107d2efbe0](https://www.nowcoder.com/practice/91b69814117f4e8097390d107d2efbe0)

``` java
public class Solution {
    public ArrayList<ArrayList<Integer> > Print(TreeNode pRoot) {
        ArrayList<ArrayList<Integer>> result = new ArrayList<>();
        if (pRoot == null) {
            return result;
        }
        LinkedList<TreeNode> queue = new LinkedList<>();
        queue.addLast(null); // 层分隔符
        queue.addLast(pRoot);
        boolean leftToRight = true;
		
        while (queue.size() != 1) {
            TreeNode node = queue.removeFirst();
            // 判断是否到达层分隔符
            if (node == null) {
                ArrayList<Integer> list = new ArrayList<>();
                Iterator<TreeNode> iterator = null;
                if (leftToRight) {
                    iterator = queue.iterator();  // 正序遍历
                } else {
                    iterator = queue.descendingIterator();  // 逆序遍历
                }
                leftToRight = !leftToRight;
                while (iterator.hasNext()) {
                    TreeNode temp = iterator.next();
                    list.add(temp.val);
                }
                result.add(list);
                queue.addLast(null);
                continue;
            }
            if (node.left != null) {
                queue.addLast(node.left);
            }
            if (node.right != null) {
                queue.addLast(node.right);
            }
        }
		
        return result;
    }
}
```

### 60. 把二叉树打印成多行

#### 题目描述

> 从上到下按层打印二叉树，同一层结点从左至右输出。每一层输出一行
> 
> 题目链接：[https://www.nowcoder.com/practice/445c44d982d04483b04a54f298796288](https://www.nowcoder.com/practice/445c44d982d04483b04a54f298796288)

``` java
public class Solution {
    private ArrayList<ArrayList<Integer>> result = new ArrayList<>();
	
    ArrayList<ArrayList<Integer> > Print(TreeNode pRoot) {
        depth(pRoot, 1);
        return result;
    }
	
    private void depth(TreeNode root, int depth) {
        if (root == null) {
            return;
        }
        if (depth > result.size()) {
            result.add(new ArrayList<>());
        }
        result.get(depth-1).add(root.val);
        depth(root.left, depth+1);
        depth(root.right, depth+1);
    } 
}
```

### 61. 序列化二叉树

#### 题目描述

> 请实现两个函数，分别用来序列化和反序列化二叉树
> 
> 题目链接：[https://www.nowcoder.com/practice/cf7e25aa97c04cc1a68c8f040e71fb84](https://www.nowcoder.com/practice/cf7e25aa97c04cc1a68c8f040e71fb84)

``` java
/**
 * 序列化就是通过先序遍历的方式，将节点拼接成一个字符串，通过逗号分隔，遇到 null 用 '#' 表示
 * 反序列化就是将拼接的字符串重新生成一个二叉树
 */
public class Solution {
    int index = -1;
    String Serialize(TreeNode root) {
        StringBuilder string = new StringBuilder();
        if (root == null) {
            string.append("#,");
            return string.toString();
        }
        string.append(root.val + ",");
        string.append(Serialize(root.left));
        string.append(Serialize(root.right));
        return string.toString();
    }
    TreeNode Deserialize(String str) {
        index++;
        String[] strings = str.split(",");
        TreeNode node = null;
        if (!"#".equals(strings[index])) {
            node = new TreeNode(Integer.valueOf(strings[index]));
            node.left = Deserialize(str);
            node.right = Deserialize(str);
        }
        return node;
    }
}
```

### 62. 二叉搜索树的第k个结点

#### 题目描述

> 给定一棵二叉搜索树，请找出其中的第k小的结点  
> 例如，（5，3，7，2，4，6，8）中，按结点数值大小顺序第三小结点的值为4  
> 
> 题目链接：[https://www.nowcoder.com/practice/ef068f602dde4d28aab2b210e859150a](https://www.nowcoder.com/practice/ef068f602dde4d28aab2b210e859150a)

``` java
/**
 * 中序遍历，递归寻找
 */
public class Solution {
    int count = 0;
    TreeNode KthNode(TreeNode pRoot, int k) {
        if (pRoot == null) {
            return null;
        }
        TreeNode node = KthNode(pRoot.left, k);
        if (node != null) {
            return node;
        }
        if (++count == k) {
            return pRoot;
        }
        node = KthNode(pRoot.right, k);
        if (node != null) {
            return node;
        }
        return null;
    }
}
```

### 63.数据流中的中位数

#### 题目描述

> 如何得到一个数据流中的中位数？  
> 如果从数据流中读出奇数个数值，那么中位数就是所有数值排序之后位于中间的数值;  
> 如果从数据流中读出偶数个数值，那么中位数就是所有数值排序之后中间两个数的平均值;  
> 我们使用Insert()方法读取数据流，使用GetMedian()方法获取当前读取数据的中位数。
> 
> 题目链接：[https://www.nowcoder.com/practice/9be0172896bd43948f8a32fb954e1be1](https://www.nowcoder.com/practice/9be0172896bd43948f8a32fb954e1be1)

#### 解题思路

``` java
import java.util.PriorityQueue;
import java.util.Comparator;

public class Solution {

    private PriorityQueue<Integer> minHeap = new PriorityQueue<>();
	
    private PriorityQueue<Integer> maxHeap = new PriorityQueue<>(new Comparator<Integer>() {
        @Override
        public int compare(Integer o1, Integer o2) {
            return o2 - o1;
        }
    });
	
    int count = 0;
	
    public void Insert(Integer num) {
        if (count % 2 == 0) {
            maxHeap.offer(num);
            int max = maxHeap.poll();
            minHeap.offer(max);
        } else {
            minHeap.offer(num);
            int min = minHeap.poll();
            maxHeap.offer(min);
        }
        count ++;
    }

    public Double GetMedian() {
        if (count % 2 == 0) {
            return new Double(minHeap.peek() + maxHeap.peek()) / 2; 
        }
        return new Double(minHeap.peek());
    }
}
```

### 64. 滑动窗口的最大值

#### 题目描述

> 给定一个数组和滑动窗口的大小，找出所有滑动窗口里数值的最大值  
> 例如，如果输入数组{2,3,4,2,6,2,5,1}及滑动窗口的大小3，那么一共存在6个滑动窗口，他们的最大值分别为{4,4,6,6,6,5}； 针对数组{2,3,4,2,6,2,5,1}的滑动窗口有以下6个： {[2,3,4],2,6,2,5,1}， {2,[3,4,2],6,2,5,1}， {2,3,[4,2,6],2,5,1}， {2,3,4,[2,6,2],5,1}， {2,3,4,2,[6,2,5],1}， {2,3,4,2,6,[2,5,1]}  
> 例如，字符串"+100","5e2","-123","3.1416"和"-1E-16"都表示数值，但是"12e","1a3.14","1.2.3","+-5"和"12e+4.3"都不是  
> 
> 题目链接：[https://www.nowcoder.com/practice/1624bc35a45c42c0bc17d17fa0cba788](https://www.nowcoder.com/practice/1624bc35a45c42c0bc17d17fa0cba788)

#### 解题思路

> 滑动窗口应当是队列，但为了得到滑动窗口的最大值，队列序可以从两端删除元素，因此使用双端队列
> 原则：对新来的元素k，将其与双端队列中的元素相比较
> 1. 从队尾开始遍历，比k小的，直接移出队列（因为不再可能成为后面滑动窗口的最大值了）,
> 2. 判断队头元素是否已不在窗口之内，不在的直接移出队列
> 3. 队列的第一个元素是滑动窗口中的最大值

``` java
import java.util.ArrayList;
import java.util.LinkedList;

public class Solution {
    public ArrayList<Integer> maxInWindows(int [] num, int size) {
        if (num == null || num.length == 0 || size == 0) {
            return new ArrayList<Integer>();
        }
        ArrayList<Integer> result = new ArrayList<>();
        LinkedList<Integer> queue = new LinkedList<>();
        for (int i = 0; i < num.length; i++) {
            while (!queue.isEmpty() && num[i] > num[queue.peekLast()]) {
                queue.pollLast();
            }
            queue.addLast(i);
			
            // 判断是否有过期元素
            if (queue.peekFirst() == (i - size)) {
                queue.pollFirst();
            }
			
            // 将最大值加入结果集
            if (i >= (size - 1)) {
                result.add(num[queue.peekFirst()]);
            }
        }
        return result;
    }
}
```

### 65. 矩阵中的路径

#### 题目描述

> 请设计一个函数，用来判断在一个矩阵中是否存在一条包含某字符串所有字符的路径  
> 路径可以从矩阵中的任意一个格子开始，每一步可以在矩阵中向左，向右，向上，向下移动一个格子。如果一条路径经过了矩阵中的某一个格子，则之后不能再次进入这个格子  
> 例如 a b c e s f c s a d e e 这样的3 X 4 矩阵中包含一条字符串"bcced"的路径，但是矩阵中不包含"abcb"路径，因为字符串的第一个字符b占据了矩阵中的第一行第二个格子之后，路径不能再次进入该格子。
> 
> 题目链接：[https://www.nowcoder.com/practice/c61c6999eecb4b8f88a98f66b273a3cc](https://www.nowcoder.com/practice/c61c6999eecb4b8f88a98f66b273a3cc)

#### 解题思路

> 新建一个数据记录该格子是否遍历过，随后进行模拟即可

``` java
public class Solution {
    public boolean hasPath(char[] matrix, int rows, int cols, char[] str)
    {
        int flag[] = new int[matrix.length];
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                if (find(matrix, rows, cols, i, j, str, 0, flag)) {
                    return true;
                }
            }
        }
        return false;
    }
    
    public boolean find(char[] matrix, int rows, int cols, int i, int j, char[] str, int cur, int[] flag) {
        int index = i * cols + j;
        if (i < 0 || i >= rows || j < 0 || j >= cols || matrix[index] != str[cur] || flag[index] == 1) {
            return false;
        }
        if (cur == str.length - 1) {
            return true;
        }
        flag[index] = 1;
        if (find(matrix, rows, cols, i - 1, j, str, cur + 1, flag)
           || find(matrix, rows, cols, i + 1, j, str, cur + 1, flag)
           || find(matrix, rows, cols, i, j - 1, str, cur + 1, flag)
           || find(matrix, rows, cols, i, j + 1, str, cur + 1, flag)) {
            return true;
        }
        flag[index] = 0;
        return false;
    }
}
```

### 66. 机器人的运动范围

#### 题目描述

> 地上有一个 m 行和 n 列的方格。一个机器人从坐标 0,0 的格子开始移动，每一次只能向左，右，上，下四个方向移动一格，但是不能进入行坐标和列坐标的数位之和大于k的格子  
> 例如，当 k 为 18 时，机器人能够进入方格（35, 37），因为 3+5+3+7 = 18。但是，它不能进入方格（35,38），因为 3+5+3+8 = 19  
> 请问该机器人能够达到多少个格子？
> 
> 题目链接：[https://www.nowcoder.com/practice/6e5207314b5241fb83f2329e89fdecc8](https://www.nowcoder.com/practice/6e5207314b5241fb83f2329e89fdecc8)

#### 解题思路

> 模拟

``` java
public class Solution {
    private int count = 0;

    public int movingCount(int threshold, int rows, int cols) {
    	int[][] matrix = new int[rows][cols];
    	find(matrix, threshold, 0, 0);
    	return count;
    }

    private void find(int[][] matrix, int threshold, int row, int col) {
    	if (row < 0 || row >= matrix.length || col < 0 || col >= matrix[0].length || matrix[row][col] == 1) {
    	    return;
    	}
    	if (!checkLimit(threshold, row, col)) {
    	    return;
    	}
    	count += 1;
    	matrix[row][col] = 1;
    	find(matrix, threshold, row+1, col);
    	find(matrix, threshold, row-1, col);
    	find(matrix, threshold, row, col+1);
    	find(matrix, threshold, row, col-1);
    }

    private boolean checkLimit(int threshold, int row, int col) {
    	int count = 0;
    	while (row > 0 || col > 0) {
    	    count += row % 10;
    	    count += col % 10;
    	    row /= 10;
    	    col /= 10;
    	}
    	count += (row + col);
    	return count <= threshold;
    }
}
```