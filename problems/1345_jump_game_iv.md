
Link to the problem https://leetcode.com/problems/jump-game-iv/

Problem broken down:
1)We have an array of integer
2) Starting point: index 0 and end point: n-1 index
3) At any index i we can go one step forward or one step backward
4) Twist: We can teleport to same value regardless of index 
5) To do: Min steps needed 


Instincts/Initial Thoughts:
1) Not recursion or Dynamic Programming:No  link between consecutive index values
2) Not Backtracking friendly :Else TLE exceeded for 1 <= arr.length <= 5 * 104
3) No sliding window: Problem is based on specific jumps not sub arrays and again teleports need complete traversal
4) Looping is extremely problematic:Teleports are impossible to predict and break Sequence
5) 
