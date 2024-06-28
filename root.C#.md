---
id: fqskcrsbhwq8k3j7a4s44bh
title: C#
desc: ''
updated: 1719571442889
created: 1719569024898
---
## C# Overview

```bash
dotnet run # runs the csharp program

dotnet new console # create a new console csharp program
```

```csharp

// Program.cs
using System; // indicates that we are using dotnet namespace

namespace HelloWorld // helps organize program, prevents collisions with other namespaces in the project
{
    class Program // object oriented programs are organized in classes
    {
        static void Main(string[] args) // entry point for program
        {
            Console.WriteLine("Hello World!"); // Console object represents a terminal
            // .Writeline is a function/method of the console object
            // in C# each line ends with ; semicolon
        }
    }
}
```
