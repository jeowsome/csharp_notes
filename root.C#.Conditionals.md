---
id: xpdh4xldgzfm0675cup1aew
title: Conditionals
desc: ''
updated: 1719587256683
created: 1719587256683
---
## Conditionals `if...else` `if...else if...else`

- Program has to make decisions based on the conditions.
- Conditional statements are used to perform different actions based on different conditions.
- `If` statement is used to execute a block of code if a condition is true.
- The syntax of the `if` statement is:
  
  ```csharp
  if (condition)
  {
      // block of code to be executed if the condition is true
  }
  ```

- You can also use `else` statement to execute a block of code if the condition is false.
- `else` statement must be used after the `if` statement.
- `else` statement does not have a condition and is optional.
- The syntax of the `if...else` statement is:
  
  ```csharp
  if (condition)
  {
      // block of code to be executed if the condition is true
  }
  else
  {
      // block of code to be executed if the condition is false
  }
  ```

- You can also use `else if` statement to specify a new condition if the first condition is false.
- You can use multiple `else if` statements.
- The syntax of the `if...else if...else` statement is:
  
  ```csharp
  if (condition1)
  {
      // block of code to be executed if condition1 is true
  }
  else if (condition2)
  {
      // block of code to be executed if the condition1 is false and condition2 is true
  }
  else
  {
      // block of code to be executed if the condition1 is false and condition2 is false
  }
  ```

## Conditionals `Switch`

- `Switch` statement is used to select one of many code blocks to be executed.
- Ideally when you have multiple `else if` statements, you can use `switch` statement.
- The syntax of the `switch` statement is:
  
  ```csharp
  switch (expression)
  {
      case value1:
          // block of code to be executed if expression is equal to value1
          break;
      case value2:
          // block of code to be executed if expression is equal to value2
          break;
      default:
          // block of code to be executed if expression is not equal to any value
          break;
  }
  ```

- `Switch` statement evaluates the expression and compares it with the values of each `case`.
- If there is a match, the block of code associated with that `case` is executed.
- If there is no match, the `default` block is executed.
- `break` statement is used to exit the `switch` statement.
- If `break` statement is not used, all the code blocks after the matching `case` are executed.
- `default` statement is optional and can appear anywhere in the `switch` statement.
- `default` statement can be used for performing a default action if no `case` matches.
