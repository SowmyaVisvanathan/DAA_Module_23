# EX 5C Kadane's Algorithm
## DATE: 06-05-25
## AIM:
To write a python program to find the maximum contiguous subarray.


## Algorithm:
1. Initialize max_till_now with the first element of the array.
2. Initialize max_ending as 0 to track the current subarray sum.
3. Iterate through each element in the array:
   - Add the current element to max_ending.
   - If max_ending becomes negative, reset it to 0 (discard current subarray).
   - If max_ending is greater than max_till_now, update max_till_now.
4. After the loop ends, return max_till_now as the maximum contiguous subarray sum.
## Program:
```
/*
To implement the program to find the maximum contiguous subarray.
Developed by: Sowmya V
Register Number: 212222110045
*/
def maxSubArraySum(a,size):
    max_till_now = a[0]
    max_ending = 0
    for i in range(0, size):
        max_ending = max_ending + a[i]
        if max_ending < 0:
            max_ending = 0
        elif (max_till_now < max_ending):
            max_till_now = max_ending
    return max_till_now
    
n=int(input())  
a =[] #[-2, -3, 4, -1, -2, 1, 5, -3]
for i in range(n):
    a.append(int(input()))
  
print("Maximum contiguous sum is", maxSubArraySum(a,n))
```
## Output:
![image](https://github.com/user-attachments/assets/195d864c-9c2e-4032-b5ae-5c9eefba4c22)

## Result:
Thus the program was executed successfully for finding the maximum contiguous sum of subarray..
