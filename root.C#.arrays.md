---
id: sbn8zyk55j8xt2sithu4inr
title: arrays
desc: ''
updated: 1720180635892
created: 1720178231715
---
## Arrays

- Arrays are a collection of elements of the same type.
- Arrays are reference types.
- Arrays are fixed in size.
- To create an array, you need to specify the type of elements and the number of elements.

```csharp
// array delcaration syntax
type[] arrayName;

int[] numbers = new int[3];
```

```csharp
int[] numbers = new int[3];
numbers[0] = 1;
numbers[1] = 2;
numbers[2] = 3;

// or
int[] numbers = new int[] { 1, 2, 3 };
```

- Array class contains methods that you can use to manipulate the content, arrangement, and size of an array.

## Array.Sort and Array.Reverse Method

- The Array.Sort method sorts the elements in an array.
- By default, the Array.Sort method sorts the elements in ascending order.
- To sort the elements in descending order, you can use the Array.Reverse method after sorting the elements in ascending order.

```csharp
int[] numbers = new int[] { 3, 1, 2 };
Array.Sort(numbers); // 1, 2, 3
Array.Reverse(numbers); // 3, 2, 1
```

- When invoking .Sort() or .Reverse() on an array, the original array is modified.

## Array.Clear and Array.Resize Method

- The Array.Clear method sets a range of elements in an array to zero. It removes the contents of specific elements in your array and replace it with the array element's default value.
  - For a `string` element, the default value is `null`.
  - For a `bool` element, the default value is `false`.
  - For a `int` element, the default value is `0`.
  - It takes three arguments: the array, the start index, and the number of elements to clear.
  Example:

  ```csharp
    int[] numbers = new int[] { 1, 2, 3 };
    Array.Clear(numbers, 0, numbers.Length); // 0, 0, 0 - 0 is the starting index and numbers.Length is the number of elements to clear

    int[] numbers2 = new int[] {0, 2, 4, 6};
    Array.Clear(numbers2, 2, 1) // 0, 2, 0, 6 - 2 is the starting index and 1 is the number of elements to clear
    ```

- The Array.Resize method changes the number of elements in an array. It adds or removes elements from the array.
- It takes two arguments: the array and the new size of the array.
- The new size of the array must be greater than or equal to zero.
- If the new size is greater than the current size, the new elements are initialized to the default value of the array element type.
- If the new size is less than the current size, the elements at the end of the array are removed.
- Array.Resize method resizes the array in place. It does not create a new array.
- Array.Resize does not remove `null` elements from the array.
- Example:

```csharp
// Resizing an array with greater size
int[] numbers = new int[] { 1, 2, 3 };
Array.Resize(ref numbers, 5); // 1, 2, 3, 0, 0

// Resizing an array with lesser size
int[] numbers = new int[] { 1, 2, 3 };
Array.Resize(ref numbers, 2); // 1, 2
```

## Array.Split, Array.Join and string.ToCharArray Method

- string.ToCharArray method converts a string to a character array.
Example:

    ```csharp
    string str = "Hello";
    char[] charArray = str.ToCharArray(); // H, e, l, l, o
    ```
