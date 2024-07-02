### C# Number Types Summary: Signed vs. Unsigned

#### Signed Integer Types

1. **`sbyte`**
   - **Range**: -128 to 127
   - **Size**: 8-bit signed
   - **Definition**: `sbyte variableName = -100;`
   - **Use Case**: Small range of signed integers.

2. **`short`**
   - **Range**: -32,768 to 32,767
   - **Size**: 16-bit signed
   - **Definition**: `short variableName = -20000;`
   - **Use Case**: Small ranges of signed numbers.

3. **`int`**
   - **Range**: -2,147,483,648 to 2,147,483,647
   - **Size**: 32-bit signed
   - **Definition**: `int variableName = -100000;`
   - **Use Case**: General-purpose signed integer operations.

4. **`long`**
   - **Range**: -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807
   - **Size**: 64-bit signed
   - **Definition**: `long variableName = -10000000000L;`
   - **Use Case**: When a wider range of signed numbers is required.

#### Unsigned Integer Types

1. **`byte`**
   - **Range**: 0 to 255
   - **Size**: 8-bit unsigned
   - **Definition**: `byte variableName = 200;`
   - **Use Case**: Small data that is non-negative.

2. **`ushort`**
   - **Range**: 0 to 65,535
   - **Size**: 16-bit unsigned
   - **Definition**: `ushort variableName = 50000;`
   - **Use Case**: Larger range of non-negative numbers.

3. **`uint`**
   - **Range**: 0 to 4,294,967,295
   - **Size**: 32-bit unsigned
   - **Definition**: `uint variableName = 3000000000U;`
   - **Use Case**: Large non-negative integers.

4. **`ulong`**
   - **Range**: 0 to 18,446,744,073,709,551,615
   - **Size**: 64-bit unsigned
   - **Definition**: `ulong variableName = 10000000000000000000UL;`
   - **Use Case**: Very large non-negative integers.

#### Floating-Point Types

1. **`float`**
   - **Range**: ±1.5 x 10^−45 to ±3.4 x 10^38
   - **Precision**: 7 digits
   - **Size**: 32-bit
   - **Definition**: `float variableName = 3.14F;`
   - **Use Case**: Large ranges of values with limited precision.

2. **`double`**
   - **Range**: ±5.0 x 10^−324 to ±1.7 x 10^308
   - **Precision**: 15-16 digits
   - **Size**: 64-bit
   - **Definition**: `double variableName = 3.14;`
   - **Use Case**: Default choice for floating-point calculations, offering more precision.

#### Decimal Type

1. **`decimal`**
   - **Range**: ±1.0 x 10^-28 to ±7.9 x 10^28
   - **Precision**: 28-29 significant digits
   - **Size**: 128-bit
   - **Definition**: `decimal variableName = 3.14M;`
   - **Use Case**: Financial and monetary calculations where precision is crucial.

---

### Summary Table

| Type       | Size     | Range                                          | Definition                    | Use Case                                  |
|------------|----------|------------------------------------------------|-------------------------------|-------------------------------------------|
| `byte`     | 8-bit    | 0 to 255                                       | `byte variableName = 200;`    | Small non-negative data                   |
| `sbyte`    | 8-bit    | -128 to 127                                    | `sbyte variableName = -100;`  | Small range of signed integers            |
| `ushort`   | 16-bit   | 0 to 65,535                                    | `ushort variableName = 50000;`| Larger range of non-negative numbers      |
| `short`    | 16-bit   | -32,768 to 32,767                              | `short variableName = -20000;`| Small ranges of signed numbers            |
| `uint`     | 32-bit   | 0 to 4,294,967,295                             | `uint variableName = 3000000000U;` | Large non-negative integers        |
| `int`      | 32-bit   | -2,147,483,648 to 2,147,483,647                | `int variableName = -100000;` | General-purpose signed integer operations |
| `ulong`    | 64-bit   | 0 to 18,446,744,073,709,551,615                | `ulong variableName = 10000000000000000000UL;` | Very large non-negative integers    |
| `long`     | 64-bit   | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 | `long variableName = -10000000000L;` | Wider range of signed numbers |
| `float`    | 32-bit   | ±1.5 x 10^−45 to ±3.4 x 10^38                  | `float variableName = 3.14F;` | Large ranges with limited precision       |
| `double`   | 64-bit   | ±5.0 x 10^−324 to ±1.7 x 10^308                | `double variableName = 3.14;` | Default choice for floating-point calculations |
| `decimal`  | 128-bit  | ±1.0 x 10^-28 to ±7.9 x 10^28                  | `decimal variableName = 3.14M;` | Financial and monetary calculations      |

---

## Extra reading

[ChatGPT reagrding math in programming](https://chatgpt.com/share/d9a8ed0e-2189-4412-87c3-73c3b7d06b53)