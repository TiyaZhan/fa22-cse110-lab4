1. The bug is that the input num1 and num2 are both strings, so string concatanation happens instead of summation of integer. The result is a type string when returning. 
2. The way to fix it will be to convert both num1 and num2 to numbers using Number(). In this way, the result will be a type number and summation can happen.
![img](/explore/devtools/fix.png)
