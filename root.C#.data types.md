---
id: hs0bg61a3120pxw24wfx5cz
title: data types
desc: ''
updated: 1720114589381
created: 1720109535454
---
## What is Data

- Data is a value stored in the computer's memory as a sequence of bits.
  - a `bit` is the smallest unit of data in a computer. It can be either 0 or 1.
  - When you group 8 bits together, you get a `byte`.
    - A byte can represent 256 different values (2^8).

## Textual Data

- As a computer only understands 0s and 1s, it needs a way to represent textual data.
- The most common way to represent textual data is by using the `ASCII` (American Standard Code for Information Interchange) character encoding.
  - ASCII uses 7 bits to represent each character, which allows for 128 different characters.
  - ASCII was later extended to use 8 bits, which allows for 256 different characters.
  - The extended version is called `Extended ASCII`.
  
## Data Types

- In C#, data types are used to define the type of data that a variable can store.

### Value Types vs Reference Types

- In C#, data types can be divided into two categories:
  - `Value Types`
  - `Reference Types`
  - The main difference between the two is how they are stored in memory.
  - `Value Types` are stored on the stack, while `Reference Types` are stored on the heap.
  - `Value Types` store the actual value, while `Reference Types` store a reference to the value.
  - `Value Types` are copied when passed as arguments to methods, while `Reference Types` are passed by reference.
  - `Value Types` are destroyed when they go out of scope, while `Reference Types` are garbage collected.

## Simple Value Types

- This are a set of predefined types provided by C# as keywords.
Example:
  - `int` - is an alias for `System.Int32`
  - `float` - is an alias for `System.Single`
  - `double` - is an alias for `System.Double`
  - `char` - is an alias for `System.Char`
  - `bool` - is an alias for `System.Boolean`
  - `byte` - is an alias for `System.Byte`
  - `short` - is an alias for `System.Int16`
  - `long` - is an alias for `System.Int64`
  - `decimal` - is an alias for `System.Decimal`
  - `sbyte` - is an alias for `System.SByte`
  - `ushort` - is an alias for `System.UInt16`
  - `uint` - is an alias for `System.UInt32`
  - `ulong` - is an alias for `System.UInt64`
  - `string` - is an alias for `System.String`
  - `object` - is an alias for `System.Object`
  - `dynamic` - is an alias for `System.Object`
  - `void` - is an alias for `System.Void`
  - `null` - is an alias for `System.Null`

## Integral Types

- Integral types are used to store whole numbers.
- They can be signed or unsigned.
- Signed types can store both positive and negative values.
- Unsigned types can only store positive values.
- The size of the integral types depends on the number of bits used to represent them.
- The following table shows the integral types available in C#:
- `sbyte` - 8-bit signed integer
- `byte` - 8-bit unsigned integer
- `short` - 16-bit signed integer
- `ushort` - 16-bit unsigned integer
- `int` - 32-bit signed integer
- `uint` - 32-bit unsigned integer
- `long` - 64-bit signed integer
- `ulong` - 64-bit unsigned integer
- `char` - 16-bit Unicode character
- `bool` - 8-bit boolean value
- `decimal` - 128-bit precise decimal values with 28-29 significant digits
- `BigInteger` - Arbitrary precision integer
=

## Floating-Point Types

- Floating types are simple value types that represents number to the right of the decimal point.
- Unlike integral types, floating-point types can represent fractional numbers.

### Evaluating Floating-Point Types

- Consider first the digits of precision each type allows.
  - `precision` is the number of digits that can be stored in a floating-point type.
- Consider the manner in which the values are stored and the impact on the accuracy of the values.
  - `accuracy` is the closeness of a measured value to a standard or known value.
  - When you need a high degree of accuracy, you should use the `decimal` type.
  - When you need a high degree of precision, you should use the `double` type.
  - When you need a high degree of range, you should use the `float` type.

### Deciphering larger floating-point values

- Because floating-point can hold larger numbers with precision, their values can be represented in scientific notation using the `E` or `e` character.
- which is a shorthand way of representing a number multiplied by a power of 10.
- For example, `1.23E3` is equivalent to `1.23 * 10^3` or `1230`.
- 5E+2 would be 5 * 10^2 or 500.

## Reference Types

- References types includes all classes, interfaces, arrays, and delegates.
- Reference types are treated differently than value types.

### How Reference Types Work

- A value type stores its values directly in an area called the stack.
  - The `stack` is a memory allocated to the code that is currently running on the CPU.
  - The stack is a last-in, first-out (LIFO) data structure.
  - The stack is fast and efficient.
  - The stack is limited in size.
  - When the stack frame has finished executing, it is popped off the stack. Meaning, the memory is deallocated.
- A reference type stores a reference to its value in an area called the heap.
  - The `heap` is a memory allocated to the application.
  - The `heap` is a memory area that is shared across many applications running on the computer.
  - The heap is a large pool of memory.
  - The heap is slower than the stack.
  - The heap is not limited in size.
  - The heap is managed by the garbage collector.
  - When the reference to the value is no longer needed, the memory is deallocated by the garbage collector.
- `new` keyword is used to create an instance of a reference type.

## String Type

- The `string` type is a reference type that represents a sequence of characters.

## How to choose the right data type

- Choose the data type that meets the boundary value range requirements of your application.
- Start with choosing the data type to fit the data (not to optimize performance).
- Choose data types based on the input and output data types of library functions used.
- Choose data types based on impact to other systems.
- When in doubt, stick with the basics.
  - `int` for most whole numbers
  - `decimal` for numbers representing money
  - `bool` for true or false values
  - `string` for alphanumeric value
- Choose specialty complex types for special situations.
  - dont reinvent data types if one or more data type already exist for a given purpose
    - `byte`: working with encoded data that comes from other computer systems or using different character sets.
    - `double`: working with geometric or scientific purposes. double is used frequently when building games involving motion.
    - `System.DateTime` for a specific date and time value.
    - `System.TimeSpan` for a span of years / months / days / hours / minutes / seconds / milliseconds.
