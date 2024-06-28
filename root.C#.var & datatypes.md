---
id: 3hk9se58sdhljk6y6prmf4p
title: var & datatypes
desc: ''
updated: 1719571659587
created: 1719571659587
---
## Types and Variables

- In Csharp we specify the type of the variable
  - This helps to cut down on programming errors

### Datatypes

- Integer types
  - Represents a 32-bit signed integer, number with no decimal points.
  - Integers are used when you need to store whole numbers.
  - Integers are the most commonly used data type.

```csharp
int i = 10;
int j = 10;
```

- Float types
  - Represents a single-precision floating point number.
  - Float numbers are used when you need to store decimal numbers with smaller precision.
  - Float numbers are suffixed with `f`.

```csharp
float k = 10.0f;
float l = 2.1f;
```

- Decimal types
  - Another kind of floating point number, representing a decimal floating point number.
  - Decimal numbers are more precise than float numbers.
  - Decimal numbers are used in financial calculations.
  - Decimal numbers are suffixed with `m`.

```csharp
decimal m = 10.0m;
decimal n = 2.1m;
```

- Boolean types
  - Represents a boolean value, either true or false.

```csharp
bool o = true;
bool p = false;
```

- Char types
  - Represents a single character.
  - Single character is enclosed in single quotes.

```csharp
char q = 'a';
char r = 'b';
```

- String types
  - Represents a sequence of characters.
  - String is enclosed in double quotes.

```csharp
string s = "Hello";
string t = "World";
```

## Var - Implicitly Typed Local Variables

- Use `var` keyword to declare a variable without specifying the type.
- The type of the variable is inferred from the value assigned to it.

```csharp
var u = 10;
var v = 10.0f;
```

- The type of the variable is determined at compile time.

## Arrays

- Arrays are used to store multiple values in a single variable.
- Arrays are declared by specifying the type of the elements and the number of elements.
- The index of the array starts from 0.
- The length of the array is fixed.
- The elements of the array are accessed using the index.
- The index of the array is enclosed in square brackets.
- Arrays can't contain elements of different types.

```csharp
int[] vals = new int[5]; // array of 5 integers with default value 0
int[] w = {1, 2, 3, 4, 5}; // array of 5 integers with values 1, 2, 3, 4, 5

string[] x = new string[3]; // array of 3 strings with default value null
string[] y = {"Hello", "World", "!"}; // array of 3 strings with values "Hello", "World", "!"
```

- The length of the array can be accessed using the `Length` property.

```csharp
Console.WriteLine(vals.Length); // 5
Console.WriteLine(w.Length); // 5
Console.WriteLine(x.Length); // 3
Console.WriteLine(y.Length); // 3
```

- The elements of the array can be accessed using the index.

```csharp
Console.WriteLine(w[0]); // 1
Console.WriteLine(w[1]); // 2
Console.WriteLine(w[2]); // 3
Console.WriteLine(w[3]); // 4
```

- The elements of the array can be modified using the index.

```csharp
w[0] = 10;
Console.WriteLine(w[0]); // 10
```

- The elements of the array can be iterated using a loop.

```csharp
for (int i = 0; i < w.Length; i++)
{
    Console.WriteLine(w[i]);
}
```

- The elements of the array can be iterated using a `foreach` loop.

```csharp
foreach (int val in w)
{
    Console.WriteLine(val);
}
```

## String Formatting

- The `+` operator is used to concatenate strings.

```csharp
string name = "Alice";
string greeting = "Hello, " + name + "!";
Console.WriteLine(greeting); // Hello, Alice!
```

- Using `{}` to format strings.

```csharp
string name = "Alice";
string greeting = $"Hello, {name}!";
Console.WriteLine(greeting); // Hello, Alice!

int age = 30;
Console.WriteLine("{0} is {1} years old", name, age); // Alice is 30 years old
```

## Null Values

- A variable can be assigned a `null` value.
- `null` is used to represent the absence of a value.

```csharp
string name = null;
Console.WriteLine(name); // null
```

## Implicit Type Conversion

- Implicit type conversion is done automatically by the compiler.
- Implicit type conversion is done when the target type can hold all possible values of the source type.

```csharp
int a = 10;
float b = a; // implicit conversion from int to float
```
