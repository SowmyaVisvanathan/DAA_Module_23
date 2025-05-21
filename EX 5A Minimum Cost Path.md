# EX 5A Minimum Cost Path
## DATE: 03-05-25
## AIM:
To write a Python program using A Naive recursive implementation of Minimum Cost Path Problem.

## Algorithm
1. Define a function to find minimum cost to reach cell (m, n) from (0, 0).
2. If m or n is less than 0, return a very large number (invalid path).
3. If (m, n) is (0, 0), return the cost of this starting cell.
4. Otherwise, find minimum cost from three possible previous cells: diagonal (m-1, n-1), top (m-1, n), and left (m, n-1).
5. Add current cell cost to the minimum of those three recursive results.
6. Use a helper to find the minimum among three values.
7. Call the function with (R-1, C-1) to get the total minimum cost path.
   
## Program:
```
/*
A program to implement to find the Minimum Cost Path Problem using a  Naive recursive Approach.

Developed by: Sowmya V
Register Number: 212222110045
*/
R = int(input())
C = int(input())

import sys
def minCost(cost, m, n):
    if (n < 0 or m < 0):
        return sys.maxsize
    elif (m == 0 and n == 0):
        return cost[m][n]
    else:
        return cost[m][n] + min( minCost(cost, m-1, n-1),
                                minCost(cost, m-1, n),
                                minCost(cost, m, n-1) )             
def min(x, y, z):
    if (x < y):
        return x if (x < z) else z
    else:
        return y if (y < z) else z
cost= [ [1, 2, 3],
        [4, 8, 2],
        [1, 5, 3] ]
print(minCost(cost, R-1, C-1))
```
## Output:
![image](https://github.com/user-attachments/assets/5cad1331-fc7d-4564-916c-977dcb530620)

## Result:
Thus the above program was executed successfully for finding the minimum cost.
