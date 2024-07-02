# Char Variables

## C# Char Type Variables Cheat Sheet

### Introduction to Char

- The `char` type in C# represents a single 16-bit Unicode character.
- It is a value type and comes under the `System.Char` structure.

### Declaring and Initializing Chars

```csharp
char a = 'a';
char number = '1';
char symbol = '$';
char unicodeChar = '\u0041';  // Unicode for 'A'
```

### Common Char Properties

- **NumericValue:** Gets the numeric value associated with the character, if any.

    ```csharp
    double numeric = char.GetNumericValue(number);  // Returns 1
    ```

### Basic Char Operations

- **Comparison:** Comparing two characters.
    
    ```csharp
    bool areEqual = (a == 'a');  // true
    ```
    
- **Conversion:** Converting a character to its uppercase or lowercase equivalent.
    
    ```csharp
    char upper = char.ToUpper(a);  // 'A'
    char lower = char.ToLower('A');  // 'a'
    ```

### Special Character Functions

- **IsDigit, IsLetter:** Checks if the character is a digit or a letter.
    
    ```csharp
    bool isDigit = char.IsDigit(number);  // true
    bool isLetter = char.IsLetter(a);  // true
    ```

### Handling Unicode Characters

- **Unicode Category:** Identifying the category of a Unicode character.

    ```csharp
    System.Globalization.UnicodeCategory category = char.GetUnicodeCategory(unicodeChar);  // UppercaseLetter
    ```

### Formatting Char

- **ToString:** Converts the `char` to a string.

    ```csharp
    string charString = a.ToString();  // "a"
    ```