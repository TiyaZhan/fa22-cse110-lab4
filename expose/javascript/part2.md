1. line 12 will print out: 3.
Since the variable `i` defined within the for loop is a var, we can still access it outside of the for loop. Since `i` is incremented by 1 every time the for loop runs, after the last iteration, i will be incremented to 3. Since `i` no longer satisfies `i < prices.length` where length is 3, `i==3` when we exit the for loop. Thus, 3 is printed out when we try to print out `i` at line 12.
2. line 13 will print out: `150`.
Since the variable `discountedPrice` is a var, we can still access it outside of the for loop. `discountedPrice` is updated everytime the for loop runs. Since the print statement at line 13 occurs after the for loop, the printed value for `discountedPrice` is set during the last iteration of the for loop. In the last iteation, `i=2`, so `discountedPrice = prices[2] * 0.5 = 150`.
3. line 14 will print out: `150`.
Since variable `finalPrice` is a var, we can access it in any scope. `finalPrice` is updated everytime the for loop runs. Since the print statement at line 14 occurs after the for loop, the printed value for `finalPrice` is set during the last iteration of the for loop. In the last iteation, `i=2`, so `finalPrice = Math.rount(150*100)/100= 150`.
4. It returns `[50, 100, 150]`. The array `discounted` is returned at the end of the function and `discounted` is a var, so it can be accessed anywhere within the function. At end of each iteration of the for loop, we add `finalPrice` into the `discounted` array. At the first iteation, `discountedPrice = price[0] *0.5 = 50` and `finalPrice = Math.rount(50*100)/100= 50`, so 50 is added into the array. At the second iteration, `discountedPrice = price[1] *0.5 = 100` and `finalPrice = Math.rount(100*100)/100= 100`, so 100 is added into the array. At the third iteration, `discountedPrice = price[2] *0.5 = 150` and `finalPrice = Math.rount(150*100)/100= 150`, so 150 is added into the array. Then, we exit the for loop and returns the array `[50, 100, 150]`.
5. The code causes an error `ReferenceError: i is not defined`. Since `i` is defined as let and is defiend within the for loop, it cannot be accessed outside of the for loop. The code at line 12 tries to access `i` outside of for loop which causes an error. 
6. The code causes an error `ReferenceError: discountedPrice is not defined`. Since `discountedPrice` is defined as let and is defiend within the for loop, it cannot be accessed outside of the for loop. The code at line 13 tries to access `discountedPrice` outside of for loop which causes an error. 
7. The line 14 will print out: `150`
Although `finalPrice` is let, it does not cause error and successfully printout the value of `finalPrice` because `finalPrice` is defined at line 4 which is the same scope/block as line 14 where the code try to access it. Since `finalPrice` is accessed at the same block as where it is defined, we successfully access it and print the value out. 
8. It returns `[50, 100, 150]`. At end of each iteration of the for loop, we add `finalPrice` into the `discounted` array. The array `discounted` is returned at the end of the function. `discounted` is let and is defined at line 3. The `return discounted` line is at the same block as where `discounted` is defined, so we can successfully access `discounted` and return it. 
9. The code causes an error `TypeError: Assignment to constant variable` at line 10. Since finalPrice is defined as const, reassignemnt is not allowed and thus, causing an error. 
10. Line 12 prints out: `3`.
length is const so it has the same scope as let. We did not try to reassign length, so it does not lead to any error about reassignemnt. Since length is defined at the same block as where we try to access it at line 12, we can successfully access length and print the value out. 
11. It returns `[50, 100, 150]`. At end of each iteration of the for loop, we add `discountedPrice` into the `discounted` array. The array `discounted` is returned at the end of the function. Adding element into the array is not reassigning the variable, so we can successfuly add element into the array even though `discounted` is a const. The `return discounted` line is at the same block as where `discounted` is defined, so we can successfully access `discounted` and return it. 
12.  
- A. `student.name`
- B. ```student['Grad Year']```
- C. `student.greeting()`
- D. `student['Favorite Teacher'].name`
- E. `student['courseLoad'][0]`

13.  
- a. '3'+2 ='32' because integers maps to their exact string representation
- b. '3' - 2 = 1 because string '3' is converted to an integer 3 and integer subtraction happens
- c. 3+null = 3 because null is converted to 0 during numeric conversion. 3+0 =3
- d. '3'+null ='3null' becuase null is converted to 'null' during string conversion
- e. true+3 = 4 because true is converted to integer 1 during the numeric conversion.
- f. false+null =0 because both false and null is converted to 0 during numeric conversion. 0+0=0
- g. '3'+undefined = '3undefined' because undefined simply maps/converts to string 'undefined' during string conversion
- h. '3'-undefined = NaN because during the numeric conversion, '3' becomes 3 and undefined becomes NaN. 3-NaN is not a valid number, so it result NaN.
14. 
- a. true, because string '2' is converted to number 2
- b. false, because '2' and '12' are both string. Based on the string comparison rules, we ony compare the first character of both strings, so '2' < '1' is false. 
- c. true, because string '2' is converted to number 2. Or if number 2 is converted to string '2', it will still return true.
- d. false, because `===` is the strict equality operater. It checks equality without type conversion. Since number 2 and string '2' are not the same type, it immediately returns false.
- e. false, becuase true is converted to integer 1 during numeric conversion. 1==2 will return false
- f. true, because 2 is a truthy values in JavaScript. Boolean(2) will return true. 
15. `===` is the strict equality operater. It checks equality without type conversion, so if a and b are different type, `===` won't convert the values and immediately returns false. However, for `==`, type conversion will happen to convert a and b to the same type. Then, compare the values of a and b. `==` will not return false only because of type differences. 
16. in part2-question16.js
17. The result will be `[2, 4, 6]`. As we call modifyArray with [1, 2, 3] and doSomething, inside the for loop of modifyArray, we call `doSomething` each time and add the return value of `doSomething` to the newArr. Since `doSomething` doubles the value of its argument and we pass in the integer at each index of [1, 2, 3] as argument during iteration of for loop,  integer at each index is doubled and added into the new Array. And the newArr is returned with the doubled value. 
18. in part2-question18.js
19. 
```
1
4
3
2
```