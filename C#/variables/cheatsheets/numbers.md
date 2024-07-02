# C# Numeric Data Types Cheat Sheet: int, float, and decimal

### Introduction to Numeric Types

- **int:** Represents a 32-bit signed integer.
- **float:** Represents a single-precision floating-point number.
- **decimal:** Represents a 128-bit precise decimal value with a larger precision and a smaller range, which makes it suitable for financial and monetary calculations.

### Declaring and Initializing Numeric Variables

```csharp
csharpCopy code
int integerNumber = 100;
float floatingNumber = 10.5f;  // Note the 'f' suffix
decimal decimalNumber = 1000.50m;  // Note the 'm' suffix

```

### Basic Numeric Operations

- **Addition, Subtraction, Multiplication, Division:**
    
    ```csharp
    int sum = 5 + 2;  // 7
    float difference = 5.5f - 2.0f;  // 3.5
    decimal product = 10m * 10m;  // 100
    float quotient = 20f / 3f;  // Approximately 6.6666665
    
    ```
    
- **Modulus:** Returns the remainder of a division.
    
    ```csharp
    int remainder = 10 % 3;  // 1
    
    ```
    

### Conversions and Casting

- **Implicit Conversion:** Automatically converting a smaller or less precise type to a larger or more precise type.
    
    ```csharp
    int num = 123;
    float numFloat = num;  // No cast needed from int to float
    
    ```
    
- **Explicit Conversion (Casting):** Required when converting a larger or more precise type to a smaller or less precise type.
    
    ```csharp
    float f = 123.456f;
    int integer = (int)f;  // Casting float to int
    
    ```
    

### Useful Methods and Properties

- **Math Class Methods:** Provides methods for performing mathematical functions.
    
    ```csharp
    int absVal = Math.Abs(-10);  // 10
    double sqrtVal = Math.Sqrt(16);  // 4.0
    decimal decPow = Math.Pow(2, 3);  // 8
    float roundVal = Math.Round(10.5f);  // 11
    
    ```
    
- **Comparing Values:**
    
    ```csharp
    int maxVal = Math.Max(10, 20);  // 20
    int minVal = Math.Min(10, 20);  // 10
    
    ```
    

### Checking Ranges and Precision

- **Overflow and Underflow:**
    - C# checks for overflow in checked contexts but does not check by default in unchecked contexts.
    
    ```csharp
    checked
    {
        int maxValue = int.MaxValue;
        int overflow = maxValue + 1;  // Throws OverflowException
    }
    
    ```
    
- **Decimal Precision:**
    - `decimal` is preferred for precise calculations, particularly where rounding errors in floating-point calculations are unacceptable.
    
    ```csharp
    decimal preciseCalculation = 0.1m + 0.2m;  // 0.3m, exactly
    
    ```
    

### Parsing Strings to Numbers

- **Parse and TryParse:**
    
    ```csharp
    int parsedInt = int.Parse("100");
    bool success = int.TryParse("123", out int result);  // true, result is 123
    float parsedFloat = float.Parse("10.01");
    decimal parsedDecimal = decimal.Parse("100.123");
    
    ```
    

This cheat sheet provides a quick reference for working with integer (`int`), floating-point (`float`), and decimal (`decimal`) types in C#, including basic operations, conversions, and common methods from the `Math` class.