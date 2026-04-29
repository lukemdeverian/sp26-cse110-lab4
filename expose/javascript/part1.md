## 1. What is printed by line 9? If the code returns an error, explain why.
- Line 9 prints "values added: 20" since add is true.
- The code does not return an error.
## 2. What is printed by line 13? If the code returns an error, explain why.
- Line 13 prints "final result: 20".
- Because var is function-scoped, result leaks out of the if block and is still accessible on line 13.
## 3. Why should you not use var? Explain why.
- var is function-scoped, not block-scoped.
- Variables leak outside the block they're written in, causing unexpected bugs.
## 4. What is printed by line 9? If the code returns an error, explain why.
- Line 9 prints "values added: 20" since add is true.
- The code does not return an error.
## 5. What is printed by line 13? If the code returns an error, explain why.
- Line 13 returns an error.
- An error is returned because let is function-scoped and not block-scoped, so result does not leak outside of the if statement.
