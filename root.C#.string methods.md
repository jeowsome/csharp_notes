---
id: j5wmu2e4d6uwqf9pepyppp7
title: string methods
desc: ''
updated: 1720187964044
created: 1720185657125
---
## Using String.IndexOf and String.Substring Method

- The `IndexOf` method returns the index of the first occurrence of a specified character or substring within a string.
  - If the character or substring is not found, it returns -1.
  - The `IndexOf` method has several overloads that allow you to specify the starting index and the number of characters to search.
  - Example:

  ```csharp
    string text = "Hello World";
    int index = text.IndexOf("World"); // 6, 6 is the index of the first character of the substring "World"
    ```

- The `Substring` method extracts a substring from a string.
  - It takes two arguments: the starting index and the length of the substring.
  - If you only specify the starting index, it will return the substring from the starting index to the end of the string.
  - Example:

   ```csharp
    string text = "Hello World";
    string sub = text.Substring(6); // World, extracts the substring starting from index 6 to the end of the string

    string sub2 = text.Substring(6, 3); // Wor, extracts the substring starting from index 6 with a length of 3 characters
    ```

## Using String.IndexOfAny and String.LastIndexOf

- The `IndexOfAny` method returns the index of the first occurrence of any character in a specified array of characters within a string.
  - If none of the characters are found, it returns -1.
  - Example:

  ```csharp
    string text = "Hello World";
    char[] chars = { 'o', 'r', 'l' };
    int index = text.IndexOfAny(chars); // 4, 4 is the index of the first occurrence of 'o'
    ```

- The `LastIndexOf` method returns the index of the last occurrence of a specified character or substring within a string.
  - If the character or substring is not found, it returns -1.
  - Example:

  ```csharp
    string text = "Hello World";
    int index = text.LastIndexOf("o"); // 7, 7 is the index of the last occurrence of 'o'
    ```

## Using String.Remove and String.Replace

- The `Remove` method removes a specified number of characters from a string starting at a specified index.
- The `Remove` method returns a new string with the specified characters removed. Does not modify the original string unless assigned to a variable.
  - It takes two arguments: the starting index and the number of characters to remove.
  - Example:

  ```csharp
    string text = "Hello World";
    string result = text.Remove(5, 5); // Hello, removes the substring starting from index 5 with a length of 5 characters
    ```

- The `Replace` method replaces all occurrences of a specified character or substring with another character or substring.
  - It takes two arguments: the character or substring to replace and the character or substring to replace it with.
  - Example:

  ```csharp
    string text = "Hello World";
    string result = text.Replace("World", "Universe"); // Hello Universe, replaces the substring "World" with "Universe"
    ```
