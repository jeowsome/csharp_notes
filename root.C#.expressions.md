---
id: 0b0gt0lq92di3utrfhszsu8
title: expressions
desc: ''
updated: 1720016990436
created: 1720014890608
---
## Evaluate an expression

- Decision logic is used to establish alternative pathways through your code, where the decision about which path to follow is based on the evaluation of an expression.
- For example you might write some code that executes one of two paths based on users input.

### What is an expression

- An expression is any combination of values (literal or variable), operators and methods that returns a single value.
- a `statement` is a complete instruction and can contain one or more expressions.
  
Example of an expression:

```csharp
if (myName == "John") // this expression returns a single value, either true or false
```

### Methods that returns a Boolean value

- "foo".StartsWith("f") // returns true
- "foo".EndsWith("f") // returns false
- "foo".Contains("o") // returns true
- "foo".Equals("foo") // returns true
- "foo".Equals("bar") // returns false
- "foo" == "foo" // returns true
- "foo" != "foo" // returns false

### Inequality operators vs Logical negation operator

- The inequality operator `!=` is used to compare two values and returns true if they are not equal.
- The logical negation operator `!` is used to reverse the logical state of its operand. If a condition is true, then the logical negation operator will make it false.

### Ternary operator

- The ternary operator `?:` is a conditional operator that returns one of two values based on the value of a Boolean expression.
- The syntax of the ternary operator is:

```csharp
condition ? first_expression : second_expression;

// Example
int a = 10;
int b = (a == 10) ? 20 : 30; // b will be 20
```
