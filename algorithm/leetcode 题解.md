# Leetcode 题册

## 0 前言

> Leetcode 刷题的笔记，可能有些方法并不是最优解，并且应当不会写什么注释，不喜勿喷
> 
> 当前合计：43题

## 1 目录

### EASY

| 序号 | 题解 |
| :--- | :--- |
| 1 | [两数之和（Two Sum）](leetcode.md#1-两数之和) |
| 7 | [反转整数（Reverse Integer）](leetcode.md#7-反转整数) |
| 9 | [回文数（Palindrome Number）](leetcode.md#9-回文数) |
| 13 | [罗马数字转整数（Roman to Integer）](leetcode.md#13-罗马数字转整数) |
| 14 | [最长公共前缀（Longest Common Prefix）](leetcode.md#14-最长公共前缀) |
| 107 | [二叉树的层次遍历 II（Binary Tree Level Order Traversal II）](leetcode.md#107-二叉树的层次遍历-ii) |
| 189 | [旋转数组（Rotate Array）](leetcode.md#189-旋转数组) |
| 191 | [位1的个数（Number of 1 Bits）](leetcode.md#191-位1的个数) |
| 203 | [移出链表元素（Remove Linked List Elements）](leetcode.md#203-移出链表元素) |
| 204 | [计数质数（Count Primes）](leetcode.md#204-计数质数) |
| 217 | [存在重复元素（Contains Duplicate）](leetcode.md#217-存在重复元素) |
| 219 | [存在重复元素 II（Contains Duplicate II）](leetcode.md#219-存在重复元素-ii) |
| 226 | [翻转二叉树（Invert Binary Tree）](leetcode.md#226-翻转二叉树) |
| 263 | [丑数（Ugly Number）](leetcode.md#263-丑数) |

### MEDIUM

| 序号 | 题解 |
| :--- | :--- |
| 2 | [两数相加（Add Two Numbers）](leetcode.md#2-两数相加) |
| 3 | [无重复字符的最长子串（Longest Substring Without Repeating Characters）](leetcode.md#3-无重复字符的最长子串) |
| 5 | [最长回文子串（Longest Palindromic Substring）](leetcode.md#5-最长回文子串) |
| 6 | [Z字形变换（ZigZag Conversion ）](leetcode.md#6-Z字形变换) |
| 8 | [字符串转换整数（String to Integer）](leetcode.md#8-字符串转换整数) |
| 11 | [盛最多水的容器（Container With Most Water）](leetcode.md#11-盛最多水的容器) |
| 12 | [整数转罗马数字（Integer to Roman）](leetcode.md#12-整数转罗马数字) |
| 34 | [在排序数组中查找元素的第一个和最后一个位置（Find First and Last Position of Element in Sorted Array）](leetcode.md#34-在排序数组中查找元素的第一个和最后一个位置) |
| 36 | [有效的数独（Valid Sudoku）](leetcode.md#36-有效的数独) |
| 96 | [不同的二叉搜索树（Unique Binary Search Trees）](leetcode.md#96-不同的二叉搜索树) |
| 102 | [二叉树的层次遍历（Binary Tree Level Order Traversal）](leetcode.md#102-二叉树的层次遍历) |
| 103 | [二叉树的锯齿形层次遍历（Binary Tree Zigzag Level Order Traversal）](leetcode.md#103-二叉树的锯齿形层次遍历) |
| 152 | [乘积最大子序列（Maximum Product Subarray）](leetcode.md#152-乘积最大子序列) |
| 153 | [寻找旋转排序数组中的最小值（Find Minimum in Rotated Sorted Array）](leetcode.md#153-寻找旋转排序数组中的最小值) |
| 201 | [数字范围按位与（Bitwise AND of Numbers Range）](leetcode.md#201-数字范围按位与) |
| 208 | [实现 Trie (前缀树)（Implement Trie (Prefix Tree)）](leetcode.md#208-实现-trie-前缀树) |
| 209 | [长度最小的子数组（Minimum Size Subarray Sum）](leetcode.md#209-长度最小的子数组) |
| 220 | [存在重复元素 III（Contains Duplicate III）](leetcode.md#220-存在重复元素-iii) |
| 223 | [矩形面积（Rectangle Area）](leetcode.md#223-矩形面积) |
| 230 | [二叉搜索树中第K小的元素（Kth Smallest Element in a BST）](leetcode.md#230-二叉搜索树中第k小的元素) |
| 264 | [丑数 II（Ugly Number II）](leetcode.md#264-丑数-ii) |
| 274 | [H指数（H-Index）](leetcode.md#274-H指数) |
| 275 | [H指数（H-Index）](leetcode.md#275-H指数-ii) |

### HARD

| 序号 | 题解 |
| :--- | :--- |
| 4 | [两个排序数组的中位数（Median of Two Sorted Arrays）](leetcode.md#4-两个排序数组的中位数) |
| 42 | [接雨水（Trapping Rain Water）](leetcode.md#42-接雨水) |
| 99 | [恢复二叉搜索树（Recover Binary Search Tree）](leetcode.md#99-恢复二叉搜索树) |
| 146 | [LRU 缓存机制（LRU Cache）](leetcode.md#146-lru-缓存机制) |
| 239 | [滑动窗口最大值（Sliding Window Maximum）](leetcode.md#239-滑动窗口最大值) |
| 273 | [整数转换英文表示（Integer to English Words）](leetcode.md#273-整数转换英文表示) |


## 题册

### 1 两数之和

> 思路1：暴力遍历，O\(N^2\)
>
> 思路2：使用 Map 存储，遍历2遍，第一次存储值和下标，第二次寻找是否存在 target-nums\[i\]
>
> 思路3：依旧使用 Map 存储，仅遍历一遍，每一次先判断 map 中是否有 target-nums\[i\]，没有则存储并且迭代下一个元素，O\(N\)
>
> 题目链接：[https://leetcode-cn.com/problems/two-sum/description/](https://leetcode-cn.com/problems/two-sum/description/)

```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        if (nums == null || nums.length < 2) return null;
        Map<Integer, Integer> map = new HashMap<>();
        for (int i = 0; i < nums.length; i++) {
            int extra = target - nums[i];
            if (map.containsKey(extra)) {
                return new int[]{ map.get(extra), i };
            }
            map.put(nums[i], i);
        }
        return null;
    }
}
```

### 2 两数相加

> 遍历两个链表，模拟逐位相加，并且记录进位
>
> 时间复杂度：O\(Max\(m, n\)\)
>
> 题目链接：[https://leetcode-cn.com/problems/add-two-numbers/description/](https://leetcode-cn.com/problems/add-two-numbers/description/)

```java
class Solution {
    public ListNode addTwoNumbers(ListNode l1, ListNode l2) {

        if (l1 == null || l2 == null) return l1 == null ? l2 : l1;

        ListNode ans = new ListNode(-1);
        ListNode current = ans;

        int ex = 0;
        while (l1 != null || l2 != null) {
            int x = l1 != null ? l1.val : 0;
            int y = l2 != null ? l2.val : 0;
            int sum = x + y + ex;
            ex = sum / 10;
            current.next = new ListNode(sum % 10);
            current = current.next;
            l1 = l1 != null ? l1.next : l1;
            l2 = l2 != null ? l2.next : l2;
        }
        if (ex > 0) current.next = new ListNode(ex);

        return ans.next;

    }
}
```

### 3 无重复字符的最长子串

> 基于 HashMap 的一种滑动窗口思想，使用两个指针来界定左右边界
>
> 时间复杂度：O\(N\)
>
> 题目链接：[https://leetcode-cn.com/problems/longest-substring-without-repeating-characters/description/](https://leetcode-cn.com/problems/longest-substring-without-repeating-characters/description/)

```java
class Solution {
    public int lengthOfLongestSubstring(String s) {

        Map<Character, Integer> map = new HashMap<>();
        int ans = 0;
        for (int i = 0, j = 0; j < s.length(); j++) {
            char tmp = s.charAt(j);
            if (map.containsKey(tmp)) {
                i = Math.max(map.get(tmp), i);
            }
            ans = Math.max(ans, j - i + 1);
            map.put(tmp, j + 1);
        }
        return ans;
    }
}
```

### 4 两个排序数组的中位数

> 二分法查找，达到 log(m+n) 的时间复杂度
> 
> 题目链接：[https://leetcode-cn.com/problems/median-of-two-sorted-arrays/description/](https://leetcode-cn.com/problems/median-of-two-sorted-arrays/description/)

```java
class Solution {
    public double findMedianSortedArrays(int[] nums1, int[] nums2) {
        int m = nums1.length;
        int n = nums2.length;
        int len = m + n;
        if (len % 2 == 1) {
            return findkth(nums1, nums2, 0, 0, m, n, len / 2 + 1);
        } else {
            double k1 = findkth(nums1, nums2, 0, 0, m, n, len / 2);
            double k2 = findkth(nums1, nums2, 0, 0, m, n, len / 2 + 1);
            return (k1 + k2) / 2;
        }
        
    }
    
    private double findkth(int[] nums1, int[] nums2, int startA, int startB, int lenA, int lenB, int k) {

        // 保证 nums1 长度小于 num2
        if (lenA > lenB) {
            return findkth(nums2, nums1, startB, startA, lenB, lenA, k);
        }
        
        // 如果 nums1 已经为空
        if (lenA == 0 && lenB > 0) {
            return nums2[startB + k - 1];
        }
        
        // k = 1 的情况
        if (k == 1) {
            return Math.min(nums1[startA], nums2[startB]);
        }
        
        // 
        int x = Math.min(k / 2, lenA);
        int y = k - x;
        
        if (nums1[startA + x - 1] < nums2[startB + y - 1]) {
            return findkth(nums1, nums2, startA + x, startB, lenA - x, lenB, k - x);
        } else if (nums1[startA + x - 1] > nums2[startB + y - 1]) {
            return findkth(nums1, nums2, startA, startB + y, lenA, lenB - y, k - y);
        } else {
            return nums1[startA + x - 1];
        }
    }
}
```

### 5 最长回文子串

> 考虑两种可能，回文是奇数或偶数（aba或abba)
> 发
> 题目链接：[https://leetcode-cn.com/problems/longest-palindromic-substring/description/](https://leetcode-cn.com/problems/longest-palindromic-substring/description/)

```java
class Solution {
    public String longestPalindrome(String s) {
        if(s.length() < 2) return s;
		int len1 = 0, len2 = 0, len, end = 0, start = 0;
        for (int i = 0; i < s.length(); i++) {
            len1 = name(i, i+1, s);
            len2 = name(i, i, s);
            len = Math.max(len1, len2);
            if(len > (end - start)) {
                end = i + len / 2;
                start = i - (len-1) / 2;
            }
        }
        return s.substring(start, end + 1);
    }
    
	public int name(int l, int r, String s) {
        while (l >= 0 && r < s.length() && s.charAt(l) == s.charAt(r)) {
            l--;
            r++;
        }
        return r - l - 1;
    }
}
```

### 6 Z字形变换

> 题目链接：[https://leetcode-cn.com/problems/zigzag-conversion/description/](https://leetcode-cn.com/problems/zigzag-conversion/description/)

```java
class Solution {
    public String convert(String s, int numRows) {
        int len = s.length();
        int nodeLen = numRows * 2 - 2;
        String result = "";
        // 特殊情况处理
        if (len == 0 || numRows == 0 || numRows == 1) {
            return s;
        }
        for (int i = 0; i < numRows; i++) {
            int index = i;
            for (int j = i; j < len; j += nodeLen) {
                result += s.charAt(j);
                if (i != 0 && i != numRows-1 && j - 2*i + nodeLen < len)
                    result += s.charAt(j - 2*i + nodeLen);
            }
        }
        return result;
    }
}
```

### 7 反转整数

> 使用 long 作为临时变量，避免溢出，同时可进行溢出判断
> 
> 题目链接：[https://leetcode-cn.com/problems/reverse-integer/description/](https://leetcode-cn.com/problems/reverse-integer/description/)

```java
class Solution {
    public int reverse(int x) {
        long tmp = x;  // 防止结果溢出
        long result = 0;
        while (tmp != 0) {
            result = result * 10 + tmp % 10;
            tmp = tmp / 10;
        }
        // 溢出判断
        if (result < Integer.MIN_VALUE || result > Integer.MAX_VALUE) {  
            result = 0;
        }
        return (int) result;
    }
}
```

### 8 字符串转换整数

> 题目链接：[https://leetcode-cn.com/problems/string-to-integer-atoi/description/](https://leetcode-cn.com/problems/string-to-integer-atoi/description/)

```java
class Solution {
    public int myAtoi(String str) {
        
        // 转换为字符数组
        char[] atoi = str.toCharArray();
        // 记录下标
        int index = 0;
        // 是否为负数
        boolean gt = true;
        
        int number = 0;
        
        // 跳过空格
        for (; index < atoi.length; index++) {
            if (atoi[index] != ' ') break;
        }
        
        if (index >= atoi.length) return 0;
        
        // 判断第一个字符
        if (!isNum(atoi[index])) {
            if (atoi[index] == '+' || atoi[index] == '-') {
                if (atoi[index] == '-') {
                    gt = false;
                }
                index++;
                if (index >= atoi.length) return 0;
            } else {
                return 0;
            }
        }
        
        for (; index < atoi.length; index++) {
            if (isNum(atoi[index])) {
                if (number > (Integer.MAX_VALUE - (atoi[index] - '0')) / 10) {
                    return gt ? Integer.MAX_VALUE : Integer.MIN_VALUE;
                }
                number = number * 10 + (atoi[index] - '0');
            } else {
                break;
            }
        }
        return gt ? number : -number;        
    }
    
    private boolean isNum(char c) {
        if (c >= '0' && c <= '9')
            return true;
        return false;
    }
}
```

### 9 回文数

> 反转一半数字，判断反转的和未反转的是否相同  
> 时间复杂度为：O(log10(n))，空间复杂度为：O(1)
> 
> 题目链接：[https://leetcode-cn.com/problems/palindrome-number/](https://leetcode-cn.com/problems/palindrome-number/)

```java
class Solution {
    public boolean isPalindrome(int x) {
        
        if (x < 0 || (x % 10 == 0 && x != 0)) {
            return false;
        }
        
        int reverse = 0;
        while (x > reverse) {
            reverse = reverse * 10 + x % 10;
            x /= 10;
        }
        
        return x == reverse || x == reverse / 10;
        
    }
}
```

### 11 盛最多水的容器

> 双指针法
> 时间复杂度：O(N)，空间复杂度：O(1)
> 
> 题目链接：[https://leetcode-cn.com/problems/container-with-most-water/](https://leetcode-cn.com/problems/container-with-most-water/)

```java
class Solution {
    public int maxArea(int[] height) {
        
        int max = 0, l = 0, r = height.length - 1;
        while (l < r) {
            int area = (r - l) * Math.min(height[l], height[r]);
            max = Math.max(max, area);
            if (height[l] < height[r]) {
                l++;
            } else {
                r--;
            }
        }
        
        return max;
    }
}
```

### 12 整数转罗马数字

> 题目链接：[https://leetcode-cn.com/problems/integer-to-roman/](https://leetcode-cn.com/problems/integer-to-roman/)
> 
> 相关案例：[Leetcode-13：罗马数字转整数](https://leetcode-cn.com/problems/roman-to-integer/)

```java
class Solution {
    public String intToRoman(int num) {
        int[] values = { 1000, 900, 500, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1 };
        String[] romes = { "M", "CM", "D", "CD", "C", "XC", "L", "XL", "X", "IX", "V", "IV", "I" };
        StringBuilder string = new StringBuilder();
        for (int i = 0; i < values.length; i++) {
            while (num >= values[i]) {
                string.append(romes[i]);
                num -= values[i];
            }
        }
        return string.toString();
    }
}
```

### 13 罗马数字转整数

> 使用 Map 存储基本字符，根据基本原则进行转换
>
> 题目链接：[https://leetcode-cn.com/problems/roman-to-integer/](https://leetcode-cn.com/problems/roman-to-integer/)
>
> 相关案例：[Leetcode-12：整数转罗马数字](https://leetcode-cn.com/problems/integer-to-roman/)

```java
class Solution {
    public int romanToInt(String s) {
        // 存储基本字符
        Map<Character, Integer> map = new HashMap<>();
        map.put('I', 1);
        map.put('V', 5);
        map.put('X', 10);
        map.put('L', 50);
        map.put('C', 100);
        map.put('D', 500);
        map.put('M', 1000);

        int num = 0;
        int min = 1000;
        char[] array = s.toCharArray();
        for (int i = 0; i < array.length; i++) {
            if (map.get(array[i]) > min) {
                num -= map.get(array[i-1]) * 2;
            }
            min = map.get(array[i]);
            num += min;
        }
        return num;
    }
}
```

### 14 最长公共前缀

> 题目链接：[https://leetcode-cn.com/problems/longest-common-prefix/](https://leetcode-cn.com/problems/longest-common-prefix/)

```java
class Solution {
    public String longestCommonPrefix(String[] strs) {
        if (strs.length == 0) { return ""; }
        if (strs.length == 1) { return strs[0]; }
        String common_prefix = "";
        common_prefix = findPrefix(strs[0], strs[1]);
        if (common_prefix == "") { return ""; }        
        for (int i = 2; i < strs.length; i++) {
            if (strs[i].startsWith(common_prefix)) { continue; }
            common_prefix = findPrefix(common_prefix, strs[i]);
        }
        return common_prefix;
    }
    
    public String findPrefix(String string1, String string2) {
        String common_prefix = "";
        int length_1 = string1.length();
        int length_2 = string2.length();
        int length = Math.min(length_1, length_2);
        for (int i = 0; i < length; i++) {
            if (string1.charAt(i) == string2.charAt(i)) {
                common_prefix += string1.charAt(i);
            } else {
                break;
            }
        }
        return common_prefix;
    }
}
```

### 34 在排序数组中查找元素的第一个和最后一个位置

> 思路1：二分法找到任意一个 target 的下标，然后向左向右找到边界
>
> 思路2：两次二分，找到左边界和右边界
>
> 题目链接：[https://leetcode-cn.com/problems/find-first-and-last-position-of-element-in-sorted-array/description/](https://leetcode-cn.com/problems/find-first-and-last-position-of-element-in-sorted-array/description/)

```java
class Solution {
    public int[] searchRange(int[] nums, int target) {
        if (nums.length == 0 || nums == null) return new int[] { -1, -1 };
        int left = findLeft(nums, target);
        int right = findRight(nums, target);
        return new int[]{ left, right };
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

### 36 有效的数独

> 思路1：分别判断行、列、3\*3 的宫内判断，该做法时间复杂度为：O\(3 \* n^3\)
>
> 思路2：首先行列的两种判断，仅需要通过交换 i 和 j，其次再进行宫内行列转换，单独判断，时间复杂度：O\(N^3\)
>
> 题目链接：[https://leetcode-cn.com/problems/valid-sudoku/description/](https://leetcode-cn.com/problems/valid-sudoku/description/)

```java
class Solution {
    public boolean isValidSudoku(char[][] board) {

        for (int i = 0; i < 9; i++) {
            int[] map_row = new int[9];
            int[] map_col = new int[9];
            int[] map_cube = new int[9];
            for (int j = 0; j < 9; j++) {
                // 行判断
                if (board[i][j] != '.') {
                    if (map_row[board[i][j] - '1'] == 1) return false;
                    map_row[board[i][j] - '1'] = 1;
                }
                // 行列转换，列判断
                if (board[j][i] != '.') {
                    if (map_col[board[j][i] - '1'] == 1) return false;
                    map_col[board[j][i] - '1'] = 1;
                }
                // 宫内行列转换
                int row = 3 * (i / 3) + j / 3;
                int col = 3 * (i % 3) + j % 3;
                if (board[row][col] != '.') {
                    if (map_cube[board[row][col] - '1'] == 1) return false;
                    map_cube[board[row][col] - '1'] = 1;
                }
            }
        }

        return true;

    }
}
```

### 42 接雨水

> 使用两个指针，第一个从右往左记录 i - n 的峰值，第二个从左往右遍历，记录 0 - i 的峰值，并计算当前段能够放置的水量
>
> 时间复杂度：O\(N\)
>
> 题目链接：[https://leetcode-cn.com/problems/trapping-rain-water/description/](https://leetcode-cn.com/problems/trapping-rain-water/description/)

```java
class Solution {
    public int trap(int[] height) {

        if (height == null || height.length <= 2) return 0;

        int n = height.length;
        // 记录 i-n 的峰值
        int[] maxR = new int[n];
        int max = height[n-1];
        for (int i = n - 1; i >= 0; i--) {
            max = Math.max(max, height[i]);
            maxR[i] = max;
        }
        // 记录 0-i 的峰值，并进行当前段的计算
        int maxL = height[0];
        int waterSum = 0;
        for (int i = 1; i < n; i++) {
            maxL = Math.max(height[i], maxL);
            waterSum += Math.max(Math.min(maxL, maxR[i]) - height[i], 0);
        }
        return waterSum;
    }
}
```

### 96 不同的二叉搜索树

> 采用 动态规划 的思路，dp[n] = dp[k-1][i-k]\(i ∈ 1 .. n)
> 
> 题目链接：[https://leetcode-cn.com/problems/unique-binary-search-trees/description/](https://leetcode-cn.com/problems/unique-binary-search-trees/description/)

```java
class Solution {
    public int numTrees(int n) {
        if (n == 0 || n == 1) return 1;
        int[] dp = new int[n+1];
        dp[0] = dp[1] = 1;
        for (int i = 2; i <= n; i++) {
            for (int j = 1; j <= i; j++) {
                dp[i] += dp[j-1] * dp[i-j];
            }
        }
        return dp[n];
    }
}
```

### 99 恢复二叉搜索树

> 首先，二叉搜索树的中序遍历是升序有序的，在交换了其中两个值的情况下，会产生两个递减的子序列，这时我们可以认定第一个子序列的第一个元素和第二个子序列的第二个元素发生了对调。
>
> 案例：原中序遍历序列：123456 -&gt; 对调后：125436，子序列：54和43，可以看出，5和3是对调的元素
>
> PS：达到常数的空间复杂度：O\(3\)
>
> 题目链接：[https://leetcode-cn.com/problems/recover-binary-search-tree/description/](https://leetcode-cn.com/problems/recover-binary-search-tree/description/)

```java
class Solution {
    TreeNode pre = null;
    TreeNode first = null;
    TreeNode sec = null;
    public void recoverTree(TreeNode root) {
        inOrder(root);
        // swap
        int tmp = first.val;
        first.val = sec.val;
        sec.val = tmp;
    }

    private void inOrder(TreeNode root) {
        if (root == null) return;
        inOrder(root.left);
        if (pre != null) {
            if (pre.val > root.val) {
                if (first == null) {
                    first = pre;
                }
                sec = root;
            }
        }
        pre = root;
        inOrder(root.right);
    }
}
```

### 102 二叉树的层次遍历

> 递归解法
> 
> 题目链接：[https://leetcode-cn.com/problems/binary-tree-level-order-traversal/description/](https://leetcode-cn.com/problems/binary-tree-level-order-traversal/description/)

```java
class Solution {
    public List<List<Integer>> levelOrder(TreeNode root) {
        if (root == null) return new ArrayList<>();
        List<List<Integer>> list = new ArrayList<>();
        dfs(root, 0, list);
        return list;
    }
    
    private void dfs(TreeNode root, int dep, List<List<Integer>> result) {
        if (result.size() < dep+1) {
            result.add(new ArrayList<Integer>());
        }
        result.get(dep).add(root.val);
        if (root.left != null) dfs(root.left, dep+1, result);
        if (root.right != null) dfs(root.right, dep+1, result);
    }
}
```

### 103 二叉树的锯齿形层次遍历

> 递归解法，并通过层数判断正逆序；使用LinkedList的addFirst方法达到头插
> 
> 题目链接：[https://leetcode-cn.com/problems/binary-tree-zigzag-level-order-traversal/description/](https://leetcode-cn.com/problems/binary-tree-zigzag-level-order-traversal/description/)

```java
class Solution {
    public List<List<Integer>> zigzagLevelOrder(TreeNode root) {
        List<List<Integer>> result = new ArrayList<>();
        if (root == null) {
            return result;
        }
        rec(root, result, 0);
        return result;
    }
    
    private void rec(TreeNode node, List<List<Integer>> result, int level) {
        if (node == null) {
            return;
        }
        if (result.size() < level + 1) {
            result.add(new LinkedList<Integer>());
        }
        if (level % 2 != 0) {
            ((LinkedList<Integer>) result.get(level)).addFirst(node.val);
        } else {
            result.get(level).add(node.val);
        }
        rec(node.left, result, level+1);
        rec(node.right, result, level+1);
    }
}
```

### 107 二叉树的层次遍历 II

> 采用和 leetcode-102 同样的做法，递归法，并借助 Collections.reverse() 方法进行逆序
> 
> 题目链接：[https://leetcode-cn.com/problems/binary-tree-level-order-traversal-ii/description/](https://leetcode-cn.com/problems/binary-tree-level-order-traversal-ii/description/)

```java
class Solution {
    public List<List<Integer>> levelOrderBottom(TreeNode root) {
        if (root == null) return new ArrayList<>();
        List<List<Integer>> list = new ArrayList<>();
        dfs(root, 0, list);
        Collections.reverse(list);
        return list;
    }
    
    private void dfs(TreeNode root, int dep, List<List<Integer>> result) {
        if (result.size() < dep+1) {
            result.add(new ArrayList<Integer>());
        }
        result.get(dep).add(root.val);
        if (root.left != null) dfs(root.left, dep+1, result);
        if (root.right != null) dfs(root.right, dep+1, result);
    }
}
```

### 146 LRU 缓存机制

> 通过继承`LinkedHashMap`，实现重写`removeEldestEntry`方法，达到最久未使用清理的机制
> 
> 题目链接：[https://leetcode-cn.com/problems/lru-cache/description/](https://leetcode-cn.com/problems/lru-cache/description/)

```java
class LRUCache {

    private Map<Integer, Integer> map;
    private int capacity;
	
	public LRUCache(int capacity) {
		this.capacity = capacity;
		map = new LRULinkedHashMap<>(capacity);
	}
	
	public int get(int key) {
		int value = -1;
        value = map.getOrDefault(key, -1);
        return value;
	}
	
	public void put(int key, int value) {
		this.map.put(key, value);
	}
}

class LRULinkedHashMap<K, V> extends LinkedHashMap<K, V> {
    
    private int capacity = 0;
	
    LRULinkedHashMap(int capacity) {
        super(16, 0.75f, true);
        this.capacity = capacity;
    }
    
    @Override
    public boolean removeEldestEntry(Map.Entry<K, V> eldest) {
        return this.size() > this.capacity;
    }
}
```

### 152 乘积最大子序列

> 乘法的过程中，可能因为正负号导致最小（大）变成最大（小），所以同时记录最小（大）值，采用动态规划，遍历整个数组

```java
class Solution {
    public int maxProduct(int[] nums) {
        if (nums == null || nums.length == 0) return -1;
        int len = nums.length;
        int _minLast = nums[0], _maxLast = nums[0], _minCur, _maxCur;
        int res = nums[0];
        for (int i = 1; i < len; i++) {
            _maxCur = Math.max(nums[i], Math.max(_maxLast * nums[i], _minLast * nums[i]));
            _minCur = Math.min(nums[i], Math.min(_maxLast * nums[i], _minLast * nums[i]));
            _maxLast = _maxCur;
            _minLast = _minCur;
            res = Math.max(res, _maxLast);
        }
        return res;
    }
}
```

### 153 寻找旋转排序数组中的最小值

> 二分法，有序的数组变成了两段升序的子序列，每一次找中间点，如果中间点大于等于最后边的，代表转折点在中间点和右端之间，否则在左端
>
> 题目链接：[https://leetcode-cn.com/problems/find-minimum-in-rotated-sorted-array/description/](https://leetcode-cn.com/problems/find-minimum-in-rotated-sorted-array/description/)
>
> 相关题目：剑指Offer第6题，[旋转数组的最小数字](jian-zhi-offer.md#6-xuan-zhuan-shu-zu-de-zui-xiao-shu-zi)

```java
class Solution {
    public int findMin(int[] nums) {
        int low = 0;
        int high = nums.length - 1;
        if (low == high) return nums[low];
        int middle = 0;
        while (nums[low] >= nums[high]) {
            middle = (high + low) >> 1;
            if (high - low == 1) {
                middle = high;
                break;
            }
            if (nums[middle] >= nums[high]) {
                low = middle;
            } else {
                high = middle;
            }
        }
        return nums[middle];
    }
}
```

### 189 旋转数组

> 题目链接：[https://leetcode-cn.com/problems/rotate-array/description/](https://leetcode-cn.com/problems/rotate-array/description/)

```java
class Solution {
    public void rotate(int[] nums, int k) {
        k %= nums.length;
        for (int i = 0; i < k; i++) {
            int tmp = nums[0];
            for (int j = 1; j < nums.length; j++) {
                int t = nums[j];
                nums[j] = tmp;
                tmp = t;
            }
            nums[0] = tmp;
        }
    }
}
```

### 191 位1的个数

> 使用和 1 的按位与得到最右边一位是否是 1，然后循环右移，该方法时间复杂度：O\(n\)
>
> PS：注意，题目中注明 n 为无符号整数，所以使用 &gt;&gt;&gt; 操作符，并且：判断条件为 n != 0
>
> 题目链接：[https://leetcode-cn.com/problems/number-of-1-bits/description/](https://leetcode-cn.com/problems/number-of-1-bits/description/)

```java
class Solution {
    // you need to treat n as an unsigned value
    public int hammingWeight(int n) {
        int count = 0;
        while (n != 0) {
            if ((n & 1) == 1) count++;
            n >>>= 1;
        }
        return count;
    }
}
```

### 201 数字范围按位与

> 一个一个与运算，会超时；考虑每一次除以二，最后在移位回来
>
> 题目链接：[https://leetcode-cn.com/problems/bitwise-and-of-numbers-range/description/](https://leetcode-cn.com/problems/bitwise-and-of-numbers-range/description/)

```java
class Solution {
    public int rangeBitwiseAnd(int m, int n) {
        return n > m ? rangeBitwiseAnd(m >> 1, n >> 1) << 1 : m;
    }
}
```

### 203 移除链表元素

> 题目链接：[https://leetcode-cn.com/problems/remove-linked-list-elements/description/](https://leetcode-cn.com/problems/remove-linked-list-elements/description/)

```java
class Solution {
    public ListNode removeElements(ListNode head, int val) {
        if (head == null)
			return null;
		if (head.val == val) {
			head.val = -1;
		}
		ListNode cur = new ListNode(-1);
		cur.next = head;
		while (cur.next != null) {
			if (cur.next.val == val) {
				cur.next = cur.next.next;
			} else {
				cur = cur.next;
			}
		}
		return head.val == -1 ? head.next : head;
    }
}
```

### 204 计数质数

> 普通质数算法会超时（即便到 sqrt(N)），考虑使用厄拉多塞筛法
>
> 题目链接：[https://leetcode-cn.com/problems/count-primes/description/](https://leetcode-cn.com/problems/count-primes/description/)

```java
class Solution {
    public int countPrimes(int n) {
        if (n < 2) return 0;
        boolean[] isPrime = new boolean[n + 1];
        isPrime[2] = false;
        
        for (int i = 3; i < n; i++) {
            if ((i & 1) == 0) {
                isPrime[i] = true;
            } else {
                isPrime[i] = false;
            }
        }
        
        for (int i = 3; i < n; i += 2) {
            if (!isPrime[i]) {
                if (i * i > n) break;
                for (int j = 2; i * j < n; j++) {
                    isPrime[i * j] = true;
                }
            }
        }
        int count = 0;
        for (int i = 2; i < n; i++) {
            if (!isPrime[i])
                count++;
        }
        return count;
    }
}
```

### 208 实现 Trie (前缀树)

> 题目链接：[https://leetcode-cn.com/problems/implement-trie-prefix-tree/description/](https://leetcode-cn.com/problems/implement-trie-prefix-tree/description/)

```java
class Trie {

    private TrieNode root;
    
    /** Initialize your data structure here. */
    public Trie() {
        root = new TrieNode();
    }
    
    /** Inserts a word into the trie. */
    public void insert(String word) {
        TrieNode node = this.root;
        for (char c : word.toCharArray()) {
            if (node.children[c-'a'] == null) {
                node.children[c-'a'] = new TrieNode();
            }
            node = node.children[c-'a'];
        }
        node.item = word;
    }
    
    /** Returns if the word is in the trie. */
    public boolean search(String word) {
        TrieNode node = this.root;
        for (char c : word.toCharArray()) {
            if (node.children[c-'a'] == null) return false;
            node = node.children[c-'a'];
        }
        return node.item.equals(word);
    }
    
    /** Returns if there is any word in the trie that starts with the given prefix. */
    public boolean startsWith(String prefix) {
        TrieNode node = this.root;
        for (char c : prefix.toCharArray()) {
            if (node.children[c - 'a'] == null) {
                return false;
            }
            node = node.children[c - 'a'];
        }
        return true;
    }
}

class TrieNode {
    // 存储子节点
    TrieNode[] children = new TrieNode[26];
    // 存储一条记录，即对应一个单词
    String item = "";
    
    public TrieNode() {
        
    }
}
```

### 209 长度最小的子数组

> 思路：滑动窗口，窗口内 sum 保持最接近 s 的状态
>
> 题目链接：[https://leetcode-cn.com/problems/minimum-size-subarray-sum/description/](https://leetcode-cn.com/problems/minimum-size-subarray-sum/description/)

```java
class Solution {
	public int minSubArrayLen(int s, int[] nums) {
		if (nums.length == 0 || nums == null)
			return 0;
		int left = 0;
		int right = -1;
		int sum = 0;
		int minLen = Integer.MAX_VALUE;
		while (right < nums.length) {
			while (sum < s && right < nums.length) {
				sum += (++right == nums.length) ? 0 : nums[right];
			}
			if (sum >= s) {
				minLen = Math.min(minLen, right - left + 1);
				sum -= nums[left++];
			}
		}
		return minLen == Integer.MAX_VALUE ? 0 : minLen;
	}
}

```

### 217 存在重复元素

> 题目链接：[https://leetcode-cn.com/problems/contains-duplicate/description/](https://leetcode-cn.com/problems/contains-duplicate/description/)

```java
class Solution {
    public boolean containsDuplicate(int[] nums) {
        Arrays.sort(nums);
        for (int i = 0; i < nums.length-1; i++) {
            if (nums[i] == nums[i+1]) return true;
        }
        return false;
    }
}
```

### 219 存在重复元素 II

> 题目链接：[https://leetcode-cn.com/problems/contains-duplicate-ii/description/](https://leetcode-cn.com/problems/contains-duplicate-ii/description/)

```java
class Solution {
    public boolean containsNearbyDuplicate(int[] nums, int k) {
        Map<Integer, Integer> map = new HashMap<>();
        for (int i = 0; i < nums.length; i++) {
            int tmp = nums[i];
            if (map.containsKey(tmp)) {
                int idx = map.get(tmp);
                if (Math.abs(idx - i) <= k) return true;
            }
            map.put(tmp, i);
        }
        return false;
    }
}
```

### 220 存在重复元素 III

> 自己的思路：往 set 保存当前下标为：i - k+1 ~ i  的元素，并截取大小在 nums\[i\] - t ~ nums\[i\] + t 范围内的元素，进而进行判断
>
> 别人的思路：遍历数组 nums，并遍历i - i+k，进而进行判断（优化：基于一种滑动窗口的思想）

* 自己的代码

```java
class Solution {
    public boolean containsNearbyAlmostDuplicate(int[] nums, int k, int t) {
        // 输入检验，去掉不合法输入以及必然会不正确的一些输入
        if (k <= 0 || t < 0 || nums == null || nums.length <= 1) return false;
        TreeSet<Long> set = new TreeSet<>();
        for (int i = 0; i < nums.length; i++) {
            SortedSet<Long> subSet = set.subSet((long) nums[i] - t, (long) nums[i] + t + 1);
            if (!subSet.isEmpty()) {
                return true;
            }
            if (i >= k) {
                set.remove((long) nums[i - k]);
            }
            set.add((long) nums[i]);
        }
        return false;
    }
}
```

* 别人的思路（优化后的，滑动窗口思想）

```javascript
class Solution {
    public boolean containsNearbyAlmostDuplicate(int[] nums, int k, int t) {
        // 输入检验，去掉不合法输入以及必然会不正确的一些输入
        if (k <= 0 || t < 0 || nums == null || nums.length <= 1) return false;
        int i = 0, j = 1;
        while (i < nums.length - 1) {
            if (i != j && Math.abs((long) nums[i] - nums[j]) <= t)
                return true;
            if (j - i == k || j == nums.length - 1) {
                i++;
                if (t != 0)
                    j = i + 1;
            } else {
                j++;
            }
        }
        return false;
    }
}
```

### 223 矩形面积

> 题目链接：[https://leetcode-cn.com/problems/rectangle-area/description/](https://leetcode-cn.com/problems/rectangle-area/description/)

```java
class Solution {
    public int computeArea(int A, int B, int C, int D, int E, int F, int G, int H) {
        int _area_A = Math.abs(C - A) * Math.abs(D - B);
        int _area_B = Math.abs(G - E) * Math.abs(H - F);
        int _area = _area_A + _area_B;
        
        int x1 = Math.max(E, A);
        int x2 = Math.min(G, C);
        
        int y1 = Math.max(B, F);
        int y2 = Math.min(D, H);
        
        if (x2 <= x1 || y2 <= y1) return _area;
        
        int _more = Math.abs(x2 - x1) * Math.abs(y2 - y1);
        return _area - _more;
    }
}
```

### 226 翻转二叉树

> 题目链接：[https://leetcode-cn.com/problems/invert-binary-tree/description/](https://leetcode-cn.com/problems/invert-binary-tree/description/)

```java
class Solution {
    public TreeNode invertTree(TreeNode root) {
        if (root == null) return root;
        rec(root);
        return root;
    }
    
    public void rec(TreeNode root) {
        if (root == null) return;
        rec(root.left);
        rec(root.right);
        reverse(root);
    }
    
    private void reverse(TreeNode root) {
        TreeNode temp = root.left;
        root.left = root.right;
        root.right = temp;
    }
}
```

### 230 二叉搜索树中第K小的元素

> 根据二叉搜索树的特性，模拟中序遍历
>
> 方法1：直接中序遍历，然后输出第k个元素，时间复杂度：O\(N\)
>
> 方法2：一边中序，一边记录个数，达到 k 则返回，时间复杂度：O\(K\)
>
> 题目链接：[https://leetcode-cn.com/problems/kth-smallest-element-in-a-bst/description/](https://leetcode-cn.com/problems/kth-smallest-element-in-a-bst/description/)

```java
class Solution {
    private int x = 0;
    public int kthSmallest(TreeNode root, int k) {
        if (root == null) return 0;
        int a = kthSmallest(root.left, k);
        if (a != 0) {
            return a;
        }
        x++;
        if (x == k) {
            return root.val;
        }
        return kthSmallest(root.right, k); 
    }
}
```

### 239 滑动窗口最大值

> 题目链接：[https://leetcode-cn.com/problems/sliding-window-maximum/description/](https://leetcode-cn.com/problems/sliding-window-maximum/description/)

```java
class Solution {
    public int[] maxSlidingWindow(int[] nums, int k) {
        
        if (nums == null || nums.length == 0) return new int[]{};
        
        LinkedList<Integer> list = new LinkedList<>();
		int[] res = new int[nums.length - k + 1];
		
		for (int i = 0; i < nums.length; i++) {
			while (!list.isEmpty() && nums[i] >= nums[list.getLast()]) {
				list.removeLast();
			}
			list.add(i);
			
			if (i - list.getFirst() + 1 > k) {
				list.removeFirst();
			}
			if (i + 1 >= k) {
				res[i - k + 1] = nums[list.getFirst()];
			}
		}
		return res;
    }
}
```

### 263 丑数

> 题目链接：[https://leetcode-cn.com/problems/ugly-number/description/](https://leetcode-cn.com/problems/ugly-number/description/)

```java
class Solution {
    public boolean isUgly(int num) {
        if (num == 0) return false;
        while (num % 2 == 0) {
            num /= 2;
        }
        while (num % 3 == 0) {
            num /= 3;
        }
        while (num % 5 == 0) {
            num /= 5;
        }
        if (num != 1) return false;
        return true;
    }
}
```

### 264 丑数 II

> 解题思路：丑数 p = 2 ^ x + 3 ^ y + 5 ^ z，简而言之，丑数是上一个丑数乘以2或3或5得到的
> 
> 题目链接：[https://leetcode-cn.com/problems/ugly-number-ii/description/](https://leetcode-cn.com/problems/ugly-number-ii/description/)
> 同 《剑指offer》 33-丑数

```java
class Solution {
    public int nthUglyNumber(int n) {
        if (n <= 0) return 0;
        List<Integer> list = new ArrayList<>();
        list.add(1);
        
        int idx_2 = 0, idx_3 = 0, idx_5 = 0;
        while (list.size() < n) {
            int m2 = list.get(idx_2) * 2;
            int m3 = list.get(idx_3) * 3;
            int m5 = list.get(idx_5) * 5;
            int min = Math.min(m2, Math.min(m3, m5));
            list.add(min);
            if (min == m2) idx_2++;
            if (min == m3) idx_3++;
            if (min == m5) idx_5++;
        }
        return list.get(n - 1);    
    }
}
```

### 273 整数转换英文表示

> 解题思路：模拟，三位为一次
> 
> 题目链接：[https://leetcode-cn.com/problems/integer-to-english-words/description/](https://leetcode-cn.com/problems/integer-to-english-words/description/)

```java
class Solution {
    public String numberToWords(int num) {
        
        String[] units = { "", " Thousand", " Million", " Billion" };
        int i = 0;
        String res = "";
        while (num > 0) {
            int temp = num % 1000;
            if (temp > 0) {
                res = convert(temp) + units[i] + (res.length() == 0 ? "" : " " + res);
            }
            num /= 1000;
            i++;
        }
        return res.isEmpty() ? "Zero" : res;
    }
    
    private String convert(int num) {
        String res = "";
        String[] ten = { "Zero", "One", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine" };
        String[] twenty = { "Ten", "Eleven", "Twelve", "Thirteen", "Fourteen", "Fifteen", "Sixteen", "Seventeen", "Eighteen", "Nineteen" };
        String[] hundred = { "Ten", "Twenty", "Thirty", "Forty", "Fifty", "Sixty", "Seventy", "Eighty", "Ninety" };
        
        if (num > 0) {
            int temp = num / 100;
            if (temp > 0) {
                res += ten[temp] + " Hundred";
            }
            temp = num % 100;
            if (temp >= 10 && temp < 20) {
                if (!res.isEmpty()) {
                    res += " ";
                }
                res += twenty[temp % 10];
                return res;
            } else if (temp >= 20) {
                temp /= 10;
                if (!res.isEmpty()) res += " ";
                res += hundred[temp - 1];
            }
            temp = num % 10;
            if (temp > 0) {
                if (!res.isEmpty()) res += " ";
                res += ten[temp];
            }
            
        }
        return res;
    }
}
```

### 274 H指数

> 解题思路：当 N 个数排序后，在 citation[i] 的右边（包括它本身），共有 N-i 个数，这些数均 >=citation[i]，即有 N-i 个数 >=citation[i]，使 h = N-i，如果此时 citation[i] >= N-i，那么必定有 N-i个数 >= N-i，此时 N-i 就是要求的 h。因为 h 取最大值，所以 i 从 0 开始
>
> 题目链接：[https://leetcode-cn.com/problems/h-index/description/](https://leetcode-cn.com/problems/h-index/description/)

```java
class Solution {
    public int hIndex(int[] citations) {
        int len = citations.length;
        Arrays.sort(citations);
        for (int i = 0; i < len; i++) {
            if (citations[i] >= len - i) {
                return len - i;
            }
        }
        return 0;
    }
}
```

### 275 H指数 II

> 解题思路：在274原题的基础原理上，考虑使用二分，优化时间复杂度
> 
> 题目链接：[https://leetcode-cn.com/problems/h-index-ii/description/](https://leetcode-cn.com/problems/h-index-ii/description/)

```java
class Solution {
    public int hIndex(int[] citations) { 
        int len = citations.length;
        int left = 0;
        int right = len - 1;
        int result = 0;
        while (left <= right) {
            int mid = (left + right) / 2;
            if (len - mid <= citations[mid]) {
                right = mid - 1;
                result = len - mid;
            } else {
                left = mid + 1;
            }
        }
        return result;
    }
}
```
