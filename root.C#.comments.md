---
id: rw29md7j3odu8p9i8q5ojtu
title: comments
desc: ''
updated: 1719585882740
created: 1719585882740
---
## Comments

- Comments are ignored by the compiler.
- Comments are used to explain the code.
- C# supports single-line and multi-line comments.
- Single-line comments start with `//`.
- Multi-line comments start with `/*` and end with `*/`.
- XML comments are used to generate documentation. Use `///` to start an XML comment.

```csharp
// This is a single-line comment

/*
This is a multi-line comment
This is a multi-line comment
This is a multi-line comment
*/
```

- Comments can be used to prevent execution of code.

```csharp
// int x = 10;

// Console.WriteLine("Hello World!");
```

- XML comments are used to generate documentation.

```csharp
/// <summary>
/// This is a summary of the method.
/// </summary>
/// <param name="x">This is the first parameter.</param>
/// <param name="y">This is the second parameter.</param>
/// <returns>This is the return value.</returns>
public int Add(int x, int y)
{
    return x + y;
}
```
