## 1. What will happen at line 12 and why? If the code causes an error, explain why.
- Line 12 prints 3.
- i is declared with var so its function-scoped.
- This means it leaks out of the for-loop.
- The for loop ends when i is 3, hence why 3 is printed.
## 2. What will happen at line 13 and why? If the code causes an error, explain why.
- Line 13 prints 150.
- discountedPrice is declared with var inside of the for loop, so its function-scoped.
- The last value it is assigned is when i is 3, the value of prices[3] is 150 and the scalar multiplier is (1-0.5), this yields 150
## 3. What will happen at line 14 and why? If the code causes an error, explain why.
- Line 14 prints 150.
- After the loop, it holds the last calculated value: Math.round(150 * 100) / 100 = 150
- So console.log(finalPrice) prints 150
## 4. What will this function return? Give a brief explanation why. If the code causes an error, explain why.
- The function returns the array [50, 100, 150]
- Each loop iteration calculates the discounted price and pushes it to discounted:
- 100 * 0.5 = 50
- 200 * 0.5 = 100
- 300 * 0.5 = 150
- Line 16 returns these elements in an array.
## 5. What will happen at line 12 and why?  If the code causes an error, explain why. ^^^ (assume this function is being called like the others: discountPrices([100, 200, 300], 0.5)).
- Line 12 throws a ReferenceError.
- i is declared with let on line 6 inside the for loop, this means it is block-scoped.
- Therefore line 12 throws a ReferenceError because i is not defined outside the block.
## 6. What will happen at line 13 and why? If the code causes an error, explain why.
- Line 13 throws a ReferenceError.
- discountedPrice is declared with let inside the for loop, this means it is block-scoped.
- Therefore line 13 throws a ReferenceError because discountedPrice is not defined outside the block.
## 7. What will happen at line 14 and why? If the code causes an error, explain why.
- Line 14 prints 150.
- finalPrice is declared with let but it is outside the loop
- After the loop, it holds the last assigned value which is 150
## 8. What will this function return? Give a brief explanation. If the code causes an error, explain why.
- The function returns the array [50, 100, 150].
- discounted is declared with let outside the for loop
-  The loop runs 3 times, pushing each discounted price into the array:
- 100 * 0.5 = 50
- 200 * 0.5 = 100
- 300 * 0.5 = 150
- Line 16 returns [50, 100, 150]
## 9. What will happen at line 11 and why? If the code causes an error, explain why.
- Line 11 throws a ReferenceError.
- i is declared with let on line 6, inside the for loop block
- By line 11, we're outside that block so i no longer exists
- JavaScript throws a ReferenceError since i is not defined
## 10. What will happen at line 12 and why? If the code causes an error, explain why.
- Line 12 prints 3
- length is declared with const at the function level
- length was assigned prices.length, which is 3
- console.log(length) prints 3
## 11. What will this function return? Give a brief explanation. If the code causes an error, explain why.
- The function returns the array [50, 100, 150]
- discounted is declared with const at the function level
- The loop pushes 50, 100, 150 into discounted
- Line 14 returns [50, 100, 150]
## 12. Given the above Object, write the notation for:
### A. Accessing the value of the name property in the student object
- student.name // 'Sarah'

### B. Accessing the value of the Grad Year property in the student object
- student['Grad Year'] // '2022'
- Bracket notation is required because the key contains a space.

### C. Calling the function for the greeting property in the student object
- student.greeting() // prints 'Hello!'

### D. Accessing the name property of the object in the Favorite Teacher property in student
- student['Favorite Teacher'].name // 'Thomas Powell'
- Bracket notation is required for 'Favorite Teacher' because the key contains a space.

### E. Access index zero in the array of the courseLoad property of the student object
- student.courseLoad[0] // 'CSE 110'