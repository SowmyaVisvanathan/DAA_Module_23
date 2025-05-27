# EX 5B Coin Change Problem
## DATE: 19-04-25
## AIM:
To compute the fewest number of coins that we need to make up the amount given.

## Algorithm
1. Initialize dp array of size amount + 1 with infinity; set dp[0] = 0.
2. For each coin in coins:
   - For each i from coin to amount:
   - Update dp[i] = min(dp[i], dp[i - coin] + 1).
3. After filling dp, check if dp[amount] is infinity:
   - If yes, return -1 (no solution).
   - Otherwise, return dp[amount] (minimum coins needed).  

## Program:
```
/*
Create a python function to compute the fewest number of coins that we need to make up the amount given.
Developed by: Sowmya V
Register Number: 212222110045
*/

class Solution(object):
   def coinChange(self, coins, amount):
       dp = [float('inf')] * (amount + 1)
       dp[0]=0
       for coin in coins:
           for i in range(coin, amount + 1):
               dp[i] = min(dp[i], dp[i - coin] + 1)
       return dp[amount] if dp[amount]!=float('inf') else -1
ob1 = Solution()
n=int(input())
s=[]
amt=int(input())
for i in range(n):
    s.append(int(input()))


print(ob1.coinChange(s,amt))
```
## Output:
![image](https://github.com/user-attachments/assets/dcc01e57-9bd8-4aee-a7f9-2eacae692f47)

## Result:
Thus the program was executed successfully for finding the minimum number of coins required to make amount.
