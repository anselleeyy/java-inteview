---
description: Leetcode 题册
---

# Leetcode

### 0 前言

{% hint style="info" %}
Leetcode 刷题的笔记，可能有些方法并不是最优解，并且应当不会写什么注释，不喜勿喷
{% endhint %}

### 1 目录

#### EASY

| 序号 | 题解 |
| :--- | :--- |
| 1 | [两数之和](leetcode.md#1-liang-shu-zhi-he) |
| 13 | [罗马数字转整数](leetcode.md#213-leetcode-13-luo-ma-shu-zi-zhuan-zheng-shu) |

#### MEDIUM

| 序号 | 题解 |
| :--- | :--- |
| 2 | [两数相加](leetcode.md#2-liang-shu-xiang-jia) |
| 3 | [无重复字符的最长子串](leetcode.md#3-wu-zhong-fu-zi-fu-de-zui-chang-zi-chuan) |
| 36 | [有效的数独](leetcode.md#36-you-xiao-de-shu-du) |

#### HARD

| 序号 | 题解 |
| :--- | :--- |
| 42 | [接雨水](leetcode.md#42-jie-yu-shui) |

## 题册

### 1 两数之和

#### 解题思路

> 思路1：暴力遍历，O\(N^2\)
>
> 思路2：使用 Map 存储，遍历2遍，第一次存储值和下标，第二次寻找是否存在 target-nums\[i\]
>
> 思路3：依旧使用 Map 存储，仅遍历一遍，每一次先判断 map 中是否有 target-nums\[i\]，没有则存储并且迭代下一个元素，O\(N\)
>
> 题目链接：[https://leetcode-cn.com/problems/two-sum/description/](https://leetcode-cn.com/problems/two-sum/description/)

```javascript
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

```javascript
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

```javascript
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

### 13 罗马数字转整数

> 使用 Map 存储基本字符，根据基本原则进行转换
>
> 题目链接：[https://leetcode-cn.com/problems/roman-to-integer/description/](https://leetcode-cn.com/problems/roman-to-integer/description/)
>
> 相关案例：Leetcode-12：整数转罗马数字

```javascript
class Solution {
    public int romanToInt(String s) {
        // 存储基本字符
        Map<Character, Integer> map = new HashMap<>();
        map.put('I',1);
        map.put('V',5);
        map.put('X',10);
        map.put('L',50);
        map.put('C',100);
        map.put('D',500);
        map.put('M',1000);

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

### 36 有效的数独

> 思路1：分别判断行、列、3\*3 的宫内判断，该做法时间复杂度为：O\(3 \* n^3\)
>
> 思路2：首先行列的两种判断，仅需要通过交换 i 和 j，其次再进行宫内行列转换，单独判断，时间复杂度：O\(N^3\)
>
> 题目链接：[https://leetcode-cn.com/problems/valid-sudoku/description/](https://leetcode-cn.com/problems/valid-sudoku/description/)

```javascript
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

```javascript
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

