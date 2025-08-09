
Link to the problem https://leetcode.com/problems/jump-game-iv/

Problem broken down:
1)We have an array of integer
2) Starting point: index 0 and end point: n-1 index
3) At any index i we can go one step forward or one step backward
4) Twist: We can teleport to same value regardless of index 
5) To do: Min steps needed 


Instincts/Initial Thoughts:
1) recursion / DP: No clear state link between consecutive indices.
2) Not backtracking: Would exceed time limits for 1 <= arr.length <= 5*10^4.
3) Not sliding window: Movement is by discrete jumps, not contiguous subarrays; teleports require full traversal.
4) Looping issues: Teleports are unpredictable and break sequential patterns.

Core Technique
5) BFS favoured over DFS: Stepwise nature of problem.Clear start and endpoint.Each index is a node. So a main chain(index based) + sidechains (teleport).
6) Multiple paths to be tried out 1 step at a time so the first time we reach a node is the best way to reach it (Standard BFS)
7) Endless looping(to and fro teleports) and revisiting the same index through multiple means must not be allowed.
8) Count should not be global but separately updated per path

Data Structures to be used:
9) A dictionary: Key as node with additional destinations list as a value pair 
10) A queue: To ensure i+1,i-1,teleports at an index are done before further cases 
11) a tuple or list to skip visited nodes

