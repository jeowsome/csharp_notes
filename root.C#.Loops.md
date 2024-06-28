---
id: rqb3ospequ9699zcz80bj4u
title: Loops
desc: ''
updated: 1719590942844
created: 1719590942844
---
## Loops `for`

- Loops can execute a block of code as long as a specified condition is true.
- Loops are handy because they save time, reduce errors, and make the code more readable.
- `For` loop is used to execute a block of code a number of times.
- It can also be used to iterate over a collection of items.
- The syntax of the `for` loop is:

  ```csharp
  for (initialization; condition; increment)
  {
      // block of code to be executed
  }

  // initialization: Initialize the loop counter variable
    // condition: Define the condition for the loop to run
    // increment: Increase the loop counter variable

    // iterate over a collection of items
    int[] numbers = { 1, 2, 3, 4, 5 };
    for (int i = 0; i < numbers.Length; i++)
    {
        Console.WriteLine(numbers[i]);
    }
  ```

## Loops `foreach`

- `Foreach` loop is used to iterate through the items in a collection.
- It is easier to use than `for` loop when you want to iterate over all the items in a collection.
- The syntax of the `foreach` loop is:

  ```csharp
  foreach (type variable in collection)
  {
      // block of code to be executed
  }

  // type: The type of the elements in the collection
  // variable: The variable that represents the current element in the collection
  // collection: The collection to iterate over

  // iterate over a collection of items
  int[] numbers = { 1, 2, 3, 4, 5 };
  foreach (int number in numbers)
  {
      Console.WriteLine(number);
  }
  ```

## Loops `while`

- `While` loop is used to execute a block of code as long as a specified condition is true.
- It is useful when you do not know the number of times the block of code needs to be executed.
- The condition is evaluated before the execution of the block of code.
- The syntax of the `while` loop is:

  ```csharp
  while (condition)
  {
      // block of code to be executed
  }

  // condition: Define the condition for the loop to run

  // iterate over a collection of items
  int[] numbers = { 1, 2, 3, 4, 5 };
  int i = 0;
  while (i < numbers.Length)
  {
      Console.WriteLine(numbers[i]);
      i++;
  }

  string input = "";
    while (input != "quit")
    {
        Console.Write("Enter a command: ");
        input = Console.ReadLine();
        Console.WriteLine("You entered: " + input);
    }
  ```

## Loops `do...while`

- `Do...while` loop is a variant of the `while` loop.
- It is used to execute a block of code at least once, and then repeat the loop as long as a specified condition is true.
- The condition is evaluated at the bottom of the loop, which means that the block of code will always be executed at least once.

```csharp
do
{
    // block of code to be executed
}
while (condition);
```
