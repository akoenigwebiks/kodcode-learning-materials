### Introduction to Boolean (bool)

- **bool:** Represents a Boolean value, which can be either `true` or `false`. It is used to perform logical operations and control flow in programs.

### Declaring and Initializing bool Variables

```csharp
csharpCopy code
bool isTrue = true;
bool isFalse = false;

```

### Basic Boolean Operations

- **Logical AND (&&):** Returns `true` if both operands are true.
    
    ```csharp
    bool result = true && false;  // false
    
    ```
    
- **Logical OR (||):** Returns `true` if at least one of the operands is true.
    
    ```csharp
    bool result = true || false;  // true
    
    ```
    
- **Logical NOT (!):** Inverts the truth value.
    
    ```csharp
    bool notTrue = !true;  // false
    
    ```
    

### Comparison Operators

- **Equality (==):** Checks if two expressions are equal.
    
    ```csharp
    bool isEqual = (5 == 5);  // true
    
    ```
    
- **Inequality (!=):** Checks if two expressions are not equal.
    
    ```csharp
    bool isNotEqual = (5 != 4);  // true
    
    ```
    

### Conditional Statements

- **If Statement:**
    
    ```csharp
    if (isTrue)
    {
        Console.WriteLine("It is true!");
    }
    
    ```
    
- **Ternary Operator (? :):** Provides a shorthand way of writing simple if-else statements.
    
    ```csharp
    string message = isTrue ? "Yes, true!" : "No, false!";
    
    ```
    

### Common Usage

- **Controlling Loops:**
    - `while` and `do-while` loops can use `bool` expressions to control the execution flow.
    
    ```csharp
    bool keepRunning = true;
    while (keepRunning)
    {
        // loop body
        // update keepRunning to false under certain conditions to stop the loop
    }
    
    ```
    
- **Switch Statements:**
    - Although `switch` statements typically use types like `int` and `string`, `bool` can be used in conditions within `case` statements.
    
    ```csharp
    switch (isTrue)
    {
        case true:
            Console.WriteLine("True case");
            break;
        case false:
            Console.WriteLine("False case");
            break;
    }
    
    ```
    

### Boolean Parsing

- **Parsing from Strings:**
    - Convert string values "true" or "false" to their respective `bool` representations.
    
    ```csharp
    bool parsed = bool.Parse("true");  // returns true
    bool tryParseResult = bool.TryParse("false", out bool parsedValue);  // parsedValue will be false
    
    ```
    

### Handling Boolean Values in Methods

- **Methods Returning bool:**
    - Common in methods that check a condition or validate data.
    
    ```csharp
    bool IsEven(int number)
    {
        return number % 2 == 0;
    }
    
    ```
    

### Booelan expressions

Boolean expressions are used to make decisions in programming. They evaluate to either true or false.
Basic Operators:

- && - Logical AND
- || - Logical OR
- ! - Logical NOT
### Comparison Operators:
```
== - Equal to
!= - Not equal to
< - Less than
> - Greater than
<= - Less than or equal to
>= - Greater than or equal to
```
### Examples:
```csharp
bool isAdult = age >= 18;
bool canDrive = hasLicense && isAdult;
bool cannotVote = !isCitizen;
bool isTeenager = age >= 13 && age <= 19;
```

### Switch Expressions
The switch expression, introduced in C# 8, provides a more concise and expressive way to handle multiple conditional branches, compared to the traditional switch statement.
Syntax:

```csharp
var result = variable switch
{
    pattern1 => result1,
    pattern2 => result2,
    _ => defaultResult // underscore is the discard pattern, used for default
};
```
### Example Using Switch Expression:
Imagine you're calculating the cost based on a product type:
```csharp
string productType = "book";
int price = productType switch
{
    "book" => 15,
    "video" => 50,
    "magazine" => 5,
    _ => 0
};
```

### Switch Statement vs. Switch Expression

#### Switch Statement:

Traditional approach.
Can execute multiple lines of code in each case.
Requires break statements to prevent fall-through (except when using return or throwing an exception).
Switch Expression:
Introduced in C# 8, more concise and functional style.
Returns a value, making it useful for direct assignment.
Handles each case with an expression, not multiple statements.

#### Example of Switch Statement:
```csharp
switch (productType)
{
    case "book":
        price = 15;
        break;
    case "video":
        price = 50;
        break;
    case "magazine":
        price = 5;
        break;
    default:
        price = 0;
        break;
}
```

This cheat sheet can be expanded with more complex examples or additional details as needed. For instance, you could add examples using patterns with switch expressions, such as type patterns or property patterns, which are very powerful for more complex data-driven conditions.

