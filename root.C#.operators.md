---
id: 2v9g8xmo0l7sa49hymm1tiu
title: operators
desc: ''
updated: 1719577401279
created: 1719577401279
---
## Operators

- Operators are symbols that perform operations on variables and values.
- C# has a rich set of operators, including arithmetic, relational, logical, and bitwise operators.

### Arithmetic Operators

- Arithmetic operators are used to perform common mathematical operations.
- C# supports the following arithmetic operators:
- `+` Addition
- `-` Subtraction
- `*` Multiplication
- `/` Division
- `%` Modulus
- `++` Increment
- `--` Decrement

```csharp
int x = 10;
int y = 20;
int z = x + y; // 30, addition
int w = x - y; // -10, subtraction
int v = x * y; // 200, multiplication
int u = y / x; // 2, division - integer division, truncates the decimal part
int t = y % x; // 0, modulus, remainder of division
int s = x++; // 10, post-increment, x is incremented after the value is assigned to s
int r = y--; // 20, post-decrement, y is decremented after the value is assigned to r

// pre-increment, x is incremented before the value is assigned to s
int q = ++x; // 11
// pre-decrement, y is decremented before the value is assigned to r
int p = --y; // 19

// floating point division
// if either operand is a float, the result is a float
// if both operands are integers, the result is an integer
// if either operand is a double, the result is a double
// if both operands are doubles, the result is a double
// if either operand is a decimal, the result is a decimal
// if both operands are decimals, the result is a decimal

float a = 10.0f;
float b = 20.0f;
float c = b / a; // 2.0
```

### Relational Operators

- Relational operators are used to compare values.
- C# supports the following relational operators:
- `==` Equal to
- `!=` Not equal to
- `>` Greater than
- `<` Less than
- `>=` Greater than or equal to
- `<=` Less than or equal to

```csharp
int x = 10;
int y = 20;

bool a = x == y; // false, equal to
bool b = x != y; // true, not equal to
bool c = x > y; // false, greater than
bool d = x < y; // true, less than
bool e = x >= y; // false, greater than or equal to
bool f = x <= y; // true, less than or equal to
```

### Logical Operators

- Logical operators are used to combine multiple conditions.
- C# supports the following logical operators:
- `&&` Logical AND
- `||` Logical OR
- `!` Logical NOT

```csharp
bool a = true;
bool b = false;

bool c = a && b; // false, logical AND
bool d = a || b; // true, logical OR
bool e = !a; // false, logical NOT
```

### Bitwise Operators

- Bitwise operators are used to perform operations on individual bits.
- C# supports the following bitwise operators:
- `&` Bitwise AND
- `|` Bitwise OR
- `^` Bitwise XOR
- `~` Bitwise NOT
- `<<` Left shift
- `>>` Right shift

```csharp
int x = 5; // 0000 0101
int y = 3; // 0000 0011

int a = x & y; // 1, bitwise AND
int b = x | y; // 7, bitwise OR
int c = x ^ y; // 6, bitwise XOR
int d = ~x; // -6, bitwise NOT
int e = x << 1; // 10, left shift by 1
int f = x >> 1; // 2, right shift by 1
```

### Assignment Operators

- Assignment operators are used to assign values to variables.
- C# supports the following assignment operators:
- `=` Assign
- `+=` Add and assign
- `-=` Subtract and assign
- `*=` Multiply and assign
- `/=` Divide and assign
- `%=` Modulus and assign
- `&=` Bitwise AND and assign
- `|=` Bitwise OR and assign
- `^=` Bitwise XOR and assign
- `<<=` Left shift and assign
- `>>=` Right shift and assign

```csharp
int x = 10;
int y = 20;

x += y; // x = x + y
x -= y; // x = x - y
x *= y; // x = x * y
x /= y; // x = x / y
x %= y; // x = x % y
x &= y; // x = x & y
x |= y; // x = x | y
x ^= y; // x = x ^ y
x <<= 1; // x = x << 1
x >>= 1; // x = x >> 1
```

### Ternary Operator

- The ternary operator is a shorthand for an `if-else` statement.
- It has the following syntax:
- `condition ? expression1 : expression2`
- If the condition is true, `expression1` is evaluated, otherwise `expression2` is evaluated.

```csharp
int x = 10;
int y = 20;

int z = x > y ? x : y; // 20, if x > y, z = x, otherwise z = y
```

### Null-Coalescing Operator

- The null-coalescing operator is used to provide a default value for nullable types.
- It has the following syntax:
- `nullable_value ?? default_value`
- If the `nullable_value` is not `null`, it is returned, otherwise the `default_value` is returned.

```csharp
int? x = null;
int y = x ?? 10; // 10, if x is null, y = 10
```

### Type Conversion Operators

- Type conversion operators are used to convert values from one type to another.
- C# supports the following type conversion operators:
- `(type) value` Explicit conversion
- `value as type` Safe conversion

```csharp
int x = 10;
double y = (double) x; // 10.0, explicit conversion
object z = y as object; // 10.0, safe conversion
```

### Operator Precedence

- Operator precedence determines the order in which operators are evaluated.
- Operators with higher precedence are evaluated first.
- Parentheses can be used to override the default precedence.

```csharp
int x = 10 + 20 * 30; // 610, multiplication has higher precedence
int y = (10 + 20) * 30; // 900, parentheses override precedence
```

### Operator Associativity

- Operator associativity determines the order in which operators of the same precedence are evaluated.
- Left-associative operators are evaluated from left to right.
- Right-associative operators are evaluated from right to left.

```csharp
int x = 10 - 5 + 3; // 8, left-associative
int y = 10 - (5 + 3); // 2, right-associative
```

### Logical Operators Short-Circuiting

- Logical operators in C# use short-circuiting.
- If the result of a logical operation can be determined by evaluating the left operand, the right operand is not evaluated.

```csharp
bool a = true;
bool b = false;

bool c = a && b; // false, b is not evaluated
bool d = a || b; // true, b is not evaluated
```
