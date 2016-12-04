003_Longest_Substring_Without_Repeating_Characters

链接：

https://leetcode.com/problems/Longest-Substring-Without-Repeating-Characters/

题意：

从标题就可以知道题意了，是求一个字符串中最长的不含重复字符的子串。

分析：

开一个数组记录当前字符最近出现的位置，一遍算过去，更新左边界，用它计算最大值就行了。
需要花费常数的空间。

备注：

1.暴力枚举时间复杂度为o（n^3),先找出所有子串，再判断每个子串中是否有重复字符，一般情况都不会这样做。

2.哈希表可以实现快速查找，对于本题，创建一个哈希表（用来存储字符的位置），初始化时表中每个数据赋值为-1，定义两个指针start和end，用于记录当前子串开始的位置和正在考察是否重复字符的位置。当end位置的字符用hash表判断出之前有重复字符时，start的位置后移（注意后移不一定只移一位，而是移动到end位置的下一位），同时end位置后移一位继续判断，否则satrt位置不动，end后移一位。
