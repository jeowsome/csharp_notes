---
id: pk9ujf1d89qpxhltv7f7dhb
title: scope
desc: ''
updated: 1720020005839
created: 1720019230831
---
## Variable Scope

- The scope of a variable is the region of code where the variable can be accessed.
- In C#, variables can be declared in different places, and the scope of a variable is determined by where it is declared.

### Code block

- A code block is a group of statements enclosed in curly braces `{}`.
- Can also be used to control or limit variable accessiblity.
- The statements outside of a code block affect when, if, and how often the code block is executed at run time.

### Removing curly braces

- If you remove the curly braces `{}` from a code block, only the first statement after the `if`, `else`, `for`, `foreach`, `while`, or `do` keyword is considered to be inside the block.
- This can lead to unexpected behavior and bugs.
- Always use curly braces to define the scope of a code block.
Example:

```csharp
if (true)
    Console.WriteLine("Hello, World!"); // this statement is inside the if block
    Console.WriteLine("Hello, World!"); // this statement is outside the if block

string name = "steve";
if (name == "bob") Console.WriteLine("Found Bob");
else if (name == "steve") Console.WriteLine("Found Steve");
else Console.WriteLine("Found Chuck");
```

- If you realize you have only one line of code listed within the code blocks of an if-elseif-else statement, you can remove the curly braces of the code block and white space. Microsoft recommends that curly braces be used consistently for all of the code blocks of an if-elseif-else statement (either present or removed consistently).
- Only remove the curly braces of a code block when it makes the code more readable. It's always acceptable to include curly braces.
- Only remove the line feed if it makes the code more readable. Microsoft suggests that your code will be more readable when each statement is placed on its own code line.
