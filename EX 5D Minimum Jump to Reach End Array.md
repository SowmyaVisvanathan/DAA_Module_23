# EX 5D Minimum Jump to Reach End Array
## DATE: 26-04-25
## AIM:
To write a python program for finding the minimum number of jumps needed to reach end of the array using Dynamic Programming.

## Algorithm:
1. If the array length n is 1, return 0 (already at the end).
2. If the first element is 0, return infinity (cannot move anywhere).
3. Otherwise, recursively calculate the minimum jumps by trying all possible jumps from 1 to arr[0] steps ahead.
4. For each possible jump i, call the function on the subarray starting at i and add 1 to count the jump.
5. Return the minimum of all these recursive results.
6. If no valid path exists, return infinity.
## Program:
```
/*
To implement the program to finding the minimum number of jumps needed to reach end of the array.
Developed by: Sowmya V
Register Number: 212222110045
*/
def minJumps(arr, n):
    if n == 1: return 0
    if arr[0] == 0: return float('inf')
    return min((minJumps(arr[i:], n - i) + 1 for i in range(1, min(n, arr[0] + 1))), default=float('inf'))
arr = []
n = int(input()) #len(arr)
for i in range(n):
    arr.append(int(input()))
print('Minimum number of jumps to reach','end is', minJumps(arr,n))
 
```
## Output:
![image](https://github.com/user-attachments/assets/866e41a9-3327-4b63-a9e3-84649d85deb0)

## Result:
Thus the program was executed successfully for finding the minimum number of jumps to reach end.
