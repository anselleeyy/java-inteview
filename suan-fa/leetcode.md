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
| 1 | [两数之和（Two Sum）](leetcode.md#1-liang-shu-zhi-he) |
| 13 | [罗马数字转整数（Roman to Integer）](leetcode.md#13-luo-ma-shu-zi-zhuan-zheng-shu) |
| 191 | [位1的个数（Number of 1 Bits）](leetcode.md#191-wei-1-de-ge-shu) |
| 217 | [存在重复元素（Contains Duplicate）](leetcode.md#217-cun-zai-zhong-fu-yuan-su) |
| 219 | [存在重复元素（Contains Duplicate II）](leetcode.md#219-cun-zai-zhong-fu-yuan-su-ii) |

#### MEDIUM

<table>
  <thead>
    <tr>
      <th style="text-align:left">序号</th>
      <th style="text-align:left">题解</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left"><a href="leetcode.md#2-liang-shu-xiang-jia">两数相加（Add Two Numbers）</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left"><a href="leetcode.md#3-wu-zhong-fu-zi-fu-de-zui-chang-zi-chuan">无重复字符的最长子串（Longest Substring Without Repeating Characters）</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">34</td>
      <td style="text-align:left">
        <p><a href="leetcode.md#34-zai-pai-xu-shu-zu-zhong-cha-zhao-yuan-su-de-di-yi-ge-he-zui-hou-yi-ge-wei-zhi">在排序数组中查找元素的第一个和最后一个位置</a>
        </p>
        <p><a href="leetcode.md#34-zai-pai-xu-shu-zu-zhong-cha-zhao-yuan-su-de-di-yi-ge-he-zui-hou-yi-ge-wei-zhi">（Find First and Last Position of Element in Sorted Array）</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">36</td>
      <td style="text-align:left"><a href="leetcode.md#36-you-xiao-de-shu-du">有效的数独（Valid Sudoku）</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">152</td>
      <td style="text-align:left"><a href="leetcode.md#152-cheng-ji-zui-da-zi-xu-lie">乘积最大子序列（Maximum Product Subarray）</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">153</td>
      <td style="text-align:left"><a href="leetcode.md#153-xun-zhao-xuan-zhuan-pai-xu-shu-zu-zhong-de-zui-xiao-zhi">寻找旋转排序数组中的最小值（Find Minimum in Rotated Sorted Array）</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">220</td>
      <td style="text-align:left"><a href="leetcode.md#220-cun-zai-zhong-fu-yuan-su-iii">存在重复元素 III（Contains Duplicate III）</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">230</td>
      <td style="text-align:left"><a href="leetcode.md#230-er-cha-sou-suo-shu-zhong-dikxiao-de-yuan-su">二叉搜索树中第K小的元素（Kth Smallest Element in a BST）</a>
      </td>
    </tr>
  </tbody>
</table>#### HARD

| 序号 | 题解 |
| :--- | :--- |
| 42 | [接雨水（Trapping Rain Water）](leetcode.md#42-jie-yu-shui) |
| 99 | [恢复二叉搜索树（Recover Binary Search Tree）](leetcode.md#99-hui-fu-er-cha-sou-suo-shu) |

## 题册

### 1 两数之和

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

### 34 在排序数组中查找元素的第一个和最后一个位置

> 思路1：二分法找到任意一个 target 的下标，然后向左向右找到边界
>
> 思路2：两次二分，找到左边界和右边界
>
> 题目链接：[https://leetcode-cn.com/problems/find-first-and-last-position-of-element-in-sorted-array/description/](https://leetcode-cn.com/problems/find-first-and-last-position-of-element-in-sorted-array/description/)

```javascript
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

### 99 恢复二叉搜索树

> 首先，二叉搜索树的中序遍历是升序有序的，在交换了其中两个值的情况下，会产生两个递减的子序列，这时我们可以认定第一个子序列的第一个元素和第二个子序列的第二个元素发生了对调。
>
> 案例：原中序遍历序列：123456 -&gt; 对调后：125436，子序列：54和43，可以看出，5和3是对调的元素
>
> PS：达到常数的空间复杂度：O\(3\)
>
> 题目链接：[https://leetcode-cn.com/problems/recover-binary-search-tree/description/](https://leetcode-cn.com/problems/recover-binary-search-tree/description/)

```javascript
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

### 152 乘积最大子序列

> 乘法的过程中，可能因为正负号导致最小（大）变成最大（小），所以同时记录最小（大）值，采用动态规划，遍历整个数组

```javascript
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

```javascript
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

### 191 位1的个数

> 使用和 1 的按位与得到最右边一位是否是 1，然后循环右移，该方法时间复杂度：O\(n\)
>
> PS：注意，题目中注明 n 为无符号整数，所以使用 &gt;&gt;&gt; 操作符，并且：判断条件为 n != 0
>
> 题目链接：[https://leetcode-cn.com/problems/number-of-1-bits/description/](https://leetcode-cn.com/problems/number-of-1-bits/description/)

```javascript
public class Solution {
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

### 217 存在重复元素

> 题目链接：[https://leetcode-cn.com/problems/contains-duplicate/description/](https://leetcode-cn.com/problems/contains-duplicate/description/)

```javascript
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

```javascript
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

```javascript
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

### 230 二叉搜索树中第K小的元素

> 根据二叉搜索树的特性，模拟中序遍历
>
> 方法1：直接中序遍历，然后输出第k个元素，时间复杂度：O\(N\)
>
> 方法2：一边中序，一边记录个数，达到 k 则返回，时间复杂度：O\(K\)
>
> 题目链接：[https://leetcode-cn.com/problems/kth-smallest-element-in-a-bst/description/](https://leetcode-cn.com/problems/kth-smallest-element-in-a-bst/description/)

```javascript
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

