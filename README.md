# 🔢 BigInt: Custom Big Integer Library in C++

Handling integers larger than `long long int` (up to 22 digits and beyond) is not feasible using primitive types in C/C++. This project implements a custom data type called `BigInt` to perform arithmetic and mathematical operations on arbitrarily large integers.

---

## 🚀 Features

The `BigInt` class supports the following operations:

### ✅ Basic Arithmetic:
- ➕ Addition of two big integers
- ➖ Subtraction of two big integers
- ✖️ Multiplication of two big integers
- ➗ Division of two big integers
- 🧮 Modulo of two big integers

### 🔣 Mathematical Functions:
- ⬆️ Raise a big integer to a power
- 🟰 Square root (floor value) of a big integer

### 🔍 Utility Operations:
- 🔁 Post/Pre Incrementation and Decrementation
- 📏 Count number of digits
- 🔁 Convert `int` to `BigInt`
- 🧮 Comparison operators (`<`, `>`, `==`, etc.)
- 📤 Print/display big integers

---

## 🧠 Approach

- **String-based Storage**:  
  Big integers are stored as strings (in reversed order for efficiency), allowing arbitrary length numbers to be represented.

- **Manual Arithmetic Logic**:
  - **Addition/Subtraction**: Implemented using digit-by-digit carry/borrow logic (like pen-and-paper method).
  - **Multiplication**: Each digit is multiplied with the other number, and intermediate results are summed.
  - **Division & Modulo**: Implemented via repeated subtraction or long division-like technique.
  - **Power**: Using exponentiation by squaring for efficiency.
  - **Square Root**: Binary search approach for integer square root.

---

## 🧮 Applications

- 🔢 Calculating **Fibonacci numbers** for values up to `10,000` and beyond
- 🧠 Computing **Factorials** of very large numbers (up to `1,000`)
- 🧬 Finding **Catalan numbers** for values up to `1,000`
- 🔍 Working with numbers beyond 20 digits in cryptographic or combinatorial algorithms

---

## 📦 Example Usage

```cpp
BigInt a = "123456789012345678901234";
BigInt b = "987654321098765432109876";

BigInt sum = a + b;
BigInt diff = a - b;
BigInt prod = a * b;
BigInt quot = b / a;
BigInt mod = b % a;

BigInt fact100 = factorial(100);
BigInt fib1000 = fibonacci(1000);
BigInt cat500 = catalan(500);

if (a > b) {
    cout << "A is greater";
}

cout << "Digits in a: " << a.numDigits() << endl;
cout << "a^5: " << pow(a, 5) << endl;
cout << "sqrt(a): " << a.sqrt() << endl;
