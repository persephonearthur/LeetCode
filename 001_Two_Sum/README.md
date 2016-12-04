001_Two_Sum

链接：

https://leetcode.com/problems/two-sum/

题意：

一个数组中两个位置上的数的和恰为 target，求这两个位置。

分析：

暴力找过去复杂度是 O(n^2)，会 TLE。

1. 可以先排序再用双指针向中间夹逼，复杂度 O(nlogn)。
2. 可以用 Map 记录出现的数，只要判断有没有和当前的数凑成 target 的数，再找出来就行，复杂度 O(nlogn) 而不是 O(n) ，因为 Map 也要复杂度的。
3. 在 2 中的 Map 复杂度可以用数组来弥补，时间复杂度是 O(n) ，不过空间复杂度是 O(MAXN)。
