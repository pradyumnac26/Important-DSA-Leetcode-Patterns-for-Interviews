This repository contains important topic wise problems and patterns for DSA interviews

## Intervals 
| Problem | Pattern |
|--------|--------|
| [Insert Interval](https://leetcode.com/problems/insert-interval/) | Since the intervals are already sorted, First add all left-side non-overlapping intervals where intervals[i][1] < newInterval[0], then merge all overlapping intervals where `intervals[i][0] <= newInterval[1]`, and finally add the remaining right-side non-overlapping intervals.| 
| [Merge Intervals](https://leetcode.com/problems/merge-intervals/) | First we sort by start time so that intervals which can overlap come next to each other, then keep merging whenever `res[-1][1] >= start`, otherwise append a new interval because it does not overlap with the previous merged one |

## Binary Search in Rotated Sorted Array 
| Problem | Pattern |
|--------|--------|
| [Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/description/) | Binary Search + Identify Sorted Half |
| [Search in Rotated Sorted Array II](https://leetcode.com/problems/search-in-rotated-sorted-array-ii/description/) | Binary Search + Identify Sorted Half + Shrink Bounds When `left == mid == right` |
| [Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/description/) | If left half sorted → `ans = arr[low]` → go right, `else ans = arr[mid]` → go left |

## Binary Search on Answers
| Problem | Pattern |
|--------|--------|
| [Koko Eating Bananas](https://leetcode.com/problems/koko-eating-bananas/description/) | Pick `mid` speed → check if Koko can finish in `h` hours → if yes try smaller speed, else increase speed |
| [Capacity To Ship Packages Within D Days](https://leetcode.com/problems/capacity-to-ship-packages-within-d-days/description/) | Pick `mid` capacity → check if all packages can be shipped within `days` → if yes try smaller capacity, else increase capacity |
| [Find the Smallest Divisor Given a Threshold](https://leetcode.com/problems/find-the-smallest-divisor-given-a-threshold/description/) | Pick `mid` divisor → compute total rounded-up divisions → if within threshold try smaller divisor, else increase divisor |
| [Minimum Number of Days to Make m Bouquets](https://leetcode.com/problems/minimum-number-of-days-to-make-m-bouquets/description/) | Pick `mid` day → check how many bouquets can be formed by that day → if enough try smaller day, else increase day |

## Priority Queue
| Problem | Pattern |
|--------|--------|
| [Reorganize Strings](https://leetcode.com/problems/reorganize-string/description/) | Max Heap + Greedy + Hold Previous |

## Palindromic Expansion around Center
| Problem | Pattern |
|--------|--------|
| [Palindromic Substrings](https://leetcode.com/problems/palindromic-substrings/) | Expand around center, count palindromes from every index |
| [Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/) | Expand around center, track max length palindrome |



## Longest Increasing Subsequence Family

| Problem | Pattern |
|--------|--------|
| [Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/) | Classic LIS DP |
| [Number of Longest Increasing Subsequence](https://leetcode.com/problems/number-of-longest-increasing-subsequence/) | LIS length + count DP |
| [Russian Doll Envelopes](https://leetcode.com/problems/russian-doll-envelopes/) | 2D LIS reduced to 1D LIS on heights after sorting by width asc and height desc |
| [Largest Divisible Subset](https://leetcode.com/problems/largest-divisible-subset/description/) | Largest Divisible Subset → Sort + LIS-style DP on divisibility condition
| 


## Longest Common Subsequence Family

| Problem | Pattern |
|--------|--------|
| [Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/) | Classic 2D DP on two strings |
| Print Longest Common Subsequence | LCS + reconstruction from DP table |
| [Longest Common Substring](https://practice.geeksforgeeks.org/problems/longest-common-substring1452/1) | 2D DP, contiguous match (reset to 0 on mismatch) |
| [Minimum Insertions or Deletions to Convert String A to B](https://leetcode.com/problems/delete-operation-for-two-strings/description/) | n + m - (2 * LCS) |
| [Shortest Common Supersequence](https://leetcode.com/problems/shortest-common-supersequence/) | n + m - LCS / reconstruction |
| [Longest Palindromic Subsequence](https://leetcode.com/problems/longest-palindromic-subsequence/) | LCS(s, reverse(s)) |
| [Minimum Insertions to Make String Palindrome](https://leetcode.com/problems/minimum-insertion-steps-to-make-a-string-palindrome/) | n - LPS |



## Topological Sort

| Problem | Pattern |
|--------|--------|
| [Course Schedule](https://leetcode.com/problems/course-schedule/) | Detect cycle in directed graph using topological sort |
| [Course Schedule II](https://leetcode.com/problems/course-schedule-ii/) | Return topological ordering of directed graph |
| [Minimum Height Trees](https://leetcode.com/problems/minimum-height-trees/) | Peel leaves layer by layer using topological sort style trimming |
| [Find Eventual Safe States](https://leetcode.com/problems/find-eventual-safe-states/) | topological sort from terminal nodes |
| [Alien Dictionary](https://neetcode.io/problems/foreign-dictionary/question?list=neetcode150) | Build graph from character order and return topological ordering |




## Multi-Source BFS

| Problem | Pattern |
|--------|--------|
| [Rotting Oranges](https://leetcode.com/problems/rotting-oranges/) | Multi-Source BFS spread and track time  |
| [01 Matrix](https://leetcode.com/problems/01-matrix/) | Shortest distance Multi-Source BFS |

## Shortest Path BFS (unit weight graphs)

| Problem | Pattern |
|--------|--------|
| [Shortest Path in a Binary Matrix](https://leetcode.com/problems/shortest-path-in-binary-matrix/) | Shortest path BFS on explicit grid |
| [Word Ladder](https://leetcode.com/problems/word-ladder/) | Shortest path BFS on implicit graph |
| [Word Ladder II](https://leetcode.com/problems/word-ladder-ii/) | Shortest path BFS + backtracking on implicit graph |
| [Open the Lock](https://leetcode.com/problems/open-the-lock/) | Shortest path BFS on implicit graph |
| [Minimum Genetic Mutation](https://leetcode.com/problems/minimum-genetic-mutation/) | Shortest path BFS on implicit graph |


## Flood Fill

| Problem | Pattern |
|--------|--------|
| [Flood Fill](https://leetcode.com/problems/flood-fill/) | Classic Flood Fill |
| [Surrounded Regions](https://leetcode.com/problems/surrounded-regions/) | Flood Fill from Boundary |
| [Number of Enclaves](https://leetcode.com/problems/number-of-enclaves/) | Flood Fill from Boundary |

## Connected Components

| Problem | Pattern |
|--------|--------|
| [Number of Islands](https://leetcode.com/problems/number-of-islands/) | Start DFS on every unvisited cell and count |
| [Number of Provinces](https://leetcode.com/problems/number-of-provinces/) | Start DFS on every unvisited node and count |
| [Number of Connected Components in an Undirected Graph](https://leetcode.com/problems/number-of-connected-components-in-an-undirected-graph/) | Start DFS on every unvisited node and count |

## Grid DFS + Memoization 

| Problem | Pattern |
|--------|--------|
| [Unique Paths](https://leetcode.com/problems/unique-paths/) | DFS + memoization for number of ways from each cell |
| [Longest Increasing Path in a Matrix](https://leetcode.com/problems/longest-increasing-path-in-a-matrix/) | DFS + memoization for longest path starting from each cell |
| [Number of Increasing Paths in a Grid](https://leetcode.com/problems/number-of-increasing-paths-in-a-grid/) | DFS + memoization for count of paths starting from each cell |

## 1D DP Unbounded Knapsack
| Problem | Pattern |
|--------|--------|
| [Coin Change](https://leetcode.com/problems/coin-change/) | Unbounded knapsack, minimize coins |
| [Coin Change II](https://leetcode.com/problems/coin-change-ii/) | Unbounded knapsack, count combinations |
| [Perfect Squares](https://leetcode.com/problems/perfect-squares/) | Unbounded knapsack, minimize count |

## DP on Squares 

| Problem | Pattern |
|--------|--------|
| [Maximal Square](https://leetcode.com/problems/maximal-square/) | Square ending at cell = 1 + min(top, left, diagonal) |
| [Count Square Submatrices with All Ones](https://leetcode.com/problems/count-square-submatrices-with-all-ones/) | Same recurrence as maximal squares, sum all dp cells |


## Matrix with Row–Column Tracking

| Problem | Pattern |
|--------|--------|
| [Special Positions in a Binary Matrix](https://leetcode.com/problems/special-positions-in-a-binary-matrix/) | Matrix Row–Column Tracking |
| [Difference Between Ones and Zeros in Row and Column](https://leetcode.com/problems/difference-between-ones-and-zeros-in-row-and-column/) | Matrix Row–Column Tracking |
| [Set Matrix Zeroes](https://leetcode.com/problems/set-matrix-zeroes/) | Matrix Row–Column Tracking |


## Design Questions 
| Problem | Pattern |
|--------|--------|
| [LRU Cache](https://leetcode.com/problems/lru-cache/description/) | LRu Cache design | 
| [Design Twitter](https://leetcode.com/problems/design-twitter/description/) | Design twitter feed |
