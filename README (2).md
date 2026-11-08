# Count Servers that Communicate

LeetCode: https://leetcode.com/problems/count-servers-that-communicate/

Difficulty: Medium

## Problem

You are given a map of a server center, represented as an `m * n` integer matrix
`grid`, where `1` means there is a server in that cell and `0` means there is
none. Two servers communicate if they are on the same row or the same column.

Return the number of servers that communicate with at least one other server.

### Example 1

```
Input: grid = [[1,0],[0,1]]
Output: 0
```

### Example 2

```
Input: grid = [[1,0],[1,1]]
Output: 3
```

### Example 3

```
Input: grid = [[1,1,0,0],[0,0,1,0],[0,0,1,0],[0,0,0,1]]
Output: 4
```

### Constraints

- `m == grid.length`, `n == grid[i].length`
- `1 <= m, n <= 250`
- `grid[i][j]` is `0` or `1`

## Approach

1. First pass: count the servers in each row (`rows[i]`) and each column
   (`cols[j]`).
2. Second pass: a server at `(i, j)` communicates with another server exactly
   when its row or its column holds more than one server
   (`rows[i] > 1 || cols[j] > 1`). Count those servers.

## Complexity

- Time: `O(m * n)`
- Space: `O(m + n)`

## Files

- `Solution.java` — Java solution
