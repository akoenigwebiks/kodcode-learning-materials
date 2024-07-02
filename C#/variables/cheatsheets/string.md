# string variables

## C# String Type Variables Cheat Sheet

### Introduction to Strings

- A string in C# is an object of the `System.String` class that stores text as a sequence of UTF-16 characters.
- Strings in C# are immutable, meaning once created, the value of a string cannot be changed.

### Declaring and Initializing Strings

```csharp
string hello = "Hello, World!";
string emptyString = String.Empty;  // Creates an empty string
string nullString = null;  // No string object is created

```

### Common String Properties

- **Length:** Gets the number of characters in the string.
    
    ```csharp
    int length = hello.Length;  // Returns 13
    ```
    

### Basic String Operations

- **Concatenation:** Combining two or more strings into one.
    
    ```csharp
    string firstName = "John";
    string lastName = "Doe";
    string fullName = firstName + " " + lastName;  // "John Doe"
    ```
    
- **Interpolation:** Inserting values into a string literal.
    
    ```csharp
    string name = "Alice";
    string greeting = $"Hello, {name}!";  // "Hello, Alice!"    
    ```
    

### Useful String Methods

- **Substring:** Extracts a substring from a string.
    
    ```csharp
    string sub = hello.Substring(0, 5);  // "Hello"
    ```
    
- **Replace:** Replaces all occurrences of a specified string.
    
    ```csharp
    string replaced = hello.Replace("World", "there");  // "Hello, there!"
    ```
    
- **ToUpper** and **ToLower:** Converts the string to uppercase or lowercase.
    
    ```csharp
    string upper = hello.ToUpper();  // "HELLO, WORLD!"
    string lower = hello.ToLower();  // "hello, world!"
    ```
    
- **Trim:** Removes all leading and trailing whitespace from a string.
    
    ```csharp
    string extraSpace = "  hello  ";
    string trimmed = extraSpace.Trim();  // "hello"
    ```
    
- **StartsWith** and **EndsWith:** Checks if the string starts or ends with a specified string.
    
    ```csharp
    bool starts = hello.StartsWith("Hello");  // true
    bool ends = hello.EndsWith("World!");  // true
    ```
    
- **Contains:** Checks if the string contains a specified substring.
    
    ```csharp
    bool contains = hello.Contains("lo, W");  // true
    ```
    

### Comparing Strings

- **String.Equals:** Compares two strings for equality.
    
    ```csharp
    bool areEqual = String.Equals("hello", "Hello", StringComparison.OrdinalIgnoreCase);  // true
    ```
    
- **String.Compare:** Compares two strings and returns an integer indicating their relative position in the sort order.
    
    ```csharp
    int compare = String.Compare("apple", "banana");  // Negative value (apple comes before banana)
    ```
    

### Handling Null or Empty Strings

- **String.IsNullOrEmpty** and **String.IsNullOrWhiteSpace:**
    
    ```csharp
    bool isEmpty = String.IsNullOrEmpty(emptyString);  // true
    bool isNullOrWhiteSpace = String.IsNullOrWhiteSpace("  ");  // true
    ```
    

### Formatting Strings

- **String.Format:** Formats a string according to specified formatting rules.
    
    ```csharp
    string formatted = String.Format("Date: {0:yyyy-MM-dd}", DateTime.Now);  // "Date: 2023-09-10"
    ```
    

This cheat sheet provides a concise overview of handling strings in C#, covering the essential properties, methods, and techniques. It can serve as a quick reference for common string operations needed in everyday coding.