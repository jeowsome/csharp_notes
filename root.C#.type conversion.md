---
id: 2f1ibpza3kx9af7md1l9dum
title: type conversion
desc: ''
updated: 1720178176754
created: 1720171415068
---
## Type Conversion

- Type conversion is the process of converting the value of one data type to another data type.
- The technique to choose depends on your answer to the two important queastions
  - Is it possible, depending on the value, that attempting to change the value's data type would throw an exception at run time?
  - Is it possible, depending on the value, that attempting to change the value's data type would result in a loss of information?
- If you need to change a value from the original data type to a new data type and the change could produce an exception at run time, you must perform a data conversion.
  - To perform data conversion, you can use one of several techniques:
    - Use a helper method on the data type
    - Use a helper method on the variable
    - Use the `Convert` class' methods
  
## Widening and Narrowing Conversions

- In C#, there are two types of type conversions:
  - `Widening conversions`, which do not lose information. For example, converting an `int` to a `long`.
  - `Narrowing conversions`, which may lose information. For example, converting a `long` to an `int`.
    - Means that you are attempting to convert a value from a data type that can hold more information to a data type that can hold less information.
    - You may lose information such as precision. An example is converting value stored in a variable of type `decimal` into a variable of type `int`.
    - When performing a narrowing conversion, you must use a cast operator to explicitly convert the value.
  
## Implicit and Explicit Conversions

- In C#, there are two types of type conversions:
  - Implicit conversions, which do not require any special syntax to be specified. For example, converting an `int` to a `long`.
    - Implicit conversions are performed by the compiler.
    - Implicit conversions are safe and do not require any special syntax.
    - Examples of implicit conversions include:
      - Converting a `byte` to an `int`.
      - Converting an `int` to a `long`.
      - Converting a `long` to a `float`.
      - Converting a `float` to a `double`.

    ```csharp
      int i = 10;
      long l = i; // implicit conversion
    ```

  - Explicit conversions, which require a cast operator to be specified. For example, converting a `long` to an `int`.
    - Explicit conversions are performed by the programmer.
    - Explicit conversions are not safe and require a cast operator.
    - Examples of explicit conversions include:
      - Converting a `long` to an `int`.
      - Converting a `double` to an `int`.
      - Converting a `float` to an `int`.
      - Converting a `double` to a `float`.

    ```csharp
      long l = 10;
      int i = (int)l; // explicit conversion
    ```

## Performing Type Casting

- Type casting is the process of converting the value of one data type to another data type.
- In C#, you can perform type casting using the cast operator `()`.
- The syntax for type casting is as follows:

```csharp
data_type variable_name = (data_type) value;
```

### Using ToString() to convert a number to a string

- Every data type in C# has a `ToString()` method that can be used to convert the value of the data type to a string.
- The `ToString()` method is a member of the `System.Object` class, which is the base class for all data types in C#.
- On most primitives, it performs a widening conversion. While this isn't strictly necessary, it can communicate to other developer that you understand what you're doing and it is intentional.

```csharp
int first = 5;
int second = 7;
string message = first.ToString() + second.ToString();
Console.WriteLine(message); // 57
```

### Using Parse() to convert a string to a number

- Most numeric data types in C# have a `Parse()` method that can be used to convert a string to a number.
- If a string cannot be converted to a number, a `FormatException` is thrown. The compiler and runtime expects you to plan ahead and prevent `illegal` conversions.
- You can use the `TryParse()` method to convert a string to a number without throwing an exception.

```csharp
string number = "123";
string number2 = "456";

int sum = int.Parse(number) + int.Parse(number2);
Console.WriteLine(sum); // 579
```

### Using TryParse() to convert a string to a number

- The `TryParse()` method is a safer way to convert a string to a number.
- The `TryParse()` method returns a `bool` value that indicates whether the conversion was successful.
- If the conversion is successful, the converted value is stored in an `out` parameter.

```csharp
string number = "123";
string number2 = "456";

int value;

if (int.TryParse(number, out value))
{
    Console.WriteLine(value); // 123
}
else
{
    Console.WriteLine("Conversion failed");
}
```

### Convert a `string` to `int` using `Convert` class

- The `Convert` class provides a set of static methods that can be used to convert a value from one data type to another.
- The `Convert` class provides a `ToInt32()` method that can be used to convert a `string` to an `int`.
- If the conversion fails, a `FormatException` is thrown.
- `Convert` class is best for converting fractional numbers to whole numbers (`int`) because it rounds the number to the nearest whole number.

```csharp
string value = "5";
string value2 = "7";
int result = Convert.ToInt32(value) + Convert.ToInt32(value2);
Console.WriteLine(result); // 12
```

### Compare casting and converting a `decimal` into an `int`

- When you cast a `decimal` to an `int`, the value is truncated.
- When you convert a `decimal` to an `int`, the value is rounded to the nearest whole number.

```csharp
int value = int(1.5m) // casting truncates the value
Console.WriteLine(value); // 1

int value2 = Convert.ToInt32(1.5m) // converting rounds the value
Console.WriteLine(value2); // 2

int value3 = Convert.ToInt32(1.4m) // converting rounds the value
Console.WriteLine(value3); // 1
```
