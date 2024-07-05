---
id: u3te65048pl5mfjo9b8v3bu
title: string formatting
desc: ''
updated: 1720185341576
created: 1720183641504
---
## What is Composite Formatting?

- Composite formatting uses numbered placeholders to format strings.
- At runtime, the placeholders are replaced with the string representation of the corresponding argument.
- The placeholders are enclosed in braces `{}`.
- Uses the `string.Format` method to format strings.
- The `string.Format` method takes two arguments: a format string and a list of objects to format.
Example:

```csharp
string first = "Hello";
string second = "World";
string result = string.Format("{0} {1}", first, second); // Hello World
```

## What is string interpolation?

- String interpolation is a technique that simplifies string formatting.
- Instead of using a numbered placeholder, you can use a variable name enclosed in braces `{}`.
- In ordere to use string interpolation, you need to prefix the string with the `$` symbol.
- Example:

```csharp
string first = "Hello";
string second = "World";
string result = $"{first} {second}"; // Hello World
```

## Formatting Currencies

- To format a currency, you can use the `C` format specifier.
- Example:

```csharp
decimal price = 123.45m;
int discount = 10;
string result = string.Format("Price: {0:C}, Discount: {1:C}", price, discount); // Price: $123.45, Discount: $10.00
```

### Custom Currency Formatting

- You can customize the currency format by specifying the number of decimal places and the currency symbol.
- This is done by setting the culture info.
- Example:

```csharp
using System.Globalization;
decimal price = 123.45m;
int discount = 10;

CultureInfo culture = new CultureInfo("en-US");
string result = string.Format(culture, "Price: {0:C}, Discount: {1:C}", price, discount); // Price: $123.45, Discount: $10.00

// Using Philippines culture
CultureInfo culture = new CultureInfo("fil-PH");
string result = string.Format(culture, "Price: {0:C}, Discount: {1:C}", price, discount); // Price: ₱123.45, Discount: ₱10.00
```

## Formatting Numbers

- To format numbers, you can use the `N` format specifier.
- By default, the `N` format specifier formats the number with two decimal places and a comma as the thousand separator.
- If you want to display more or fewer decimal places, you can specify the number of decimal places after the `N` format specifier.
- Example:

```csharp
int number = 1234567;
string result = string.Format("Number: {0:N}", number); // Number: 1,234,567.00

// Custom number formatting
string result = string.Format("Number: {0:N3}", number); // Number: 1,234,567.000
```

## Formatting percentages

- To format percentages, you can use the `P` format specifier.
- Percentage values are multiplied by 100 and displayed with a percent sign. By default, the percentage is displayed with two decimal places.
- You can specify the number of decimal places after the `P` format specifier.

```csharp
decimal percentage = 0.1234m;
string result = string.Format("Percentage: {0:P}", percentage); // Percentage: 12.34%

// Custom percentage formatting
string result = string.Format("Percentage: {0:P2}", percentage); // Percentage: 12.34%
```
