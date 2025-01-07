# swap-2-number

### 2. Using Addition and Subtraction

```
var a = 10
var b = 20

print("Before swapping: a = \(a), b = \(b)")

a = a + b // a now becomes 30
b = a - b // b becomes 10 (original value of a)
a = a - b // a becomes 20 (original value of b)

print("After swapping: a = \(a), b = \(b)")

```

### 2. Using Multiplication and Division (Safe if Numbers Are Non-Zero)

```
var a = 10
var b = 20

print("Before swapping: a = \(a), b = \(b)")

a = a * b // a becomes 200
b = a / b // b becomes 10 (original value of a)
a = a / b // a becomes 20 (original value of b)

print("After swapping: a = \(a), b = \(b)")

```

**Note**: This method works only if both numbers are non-zero to avoid division by zero.

### 3. Using Bitwise XOR (Efficient for Integers)

```
var a = 10 // Binary: 1010
var b = 20 // Binary: 10100

print("Before swapping: a = \(a), b = \(b)")

a = a ^ b // a becomes 11110 (bitwise XOR of 1010 and 10100)
b = a ^ b // b becomes 1010 (original value of a)
a = a ^ b // a becomes 10100 (original value of b)

print("After swapping: a = \(a), b = \(b)")

```

**Note**: This method is suitable for integers and works at the bit level.

### 4. Using Swift Tuple Swapping

```
var a = 10
var b = 20

print("Before swapping: a = \(a), b = \(b)")

(a, b) = (b, a)

print("After swapping: a = \(a), b = \(b)")

```

**Note**: This is the cleanest and most idiomatic way to swap values in Swift.

Method | Performance |  Readability | Constraints
--- | --- | --- | ---
Addition/Subtraction    |  Fast         | Moderate        | Can cause overflow with large numbers.
Multiplication/Division	|  Fast	        | Moderate	      | Fails if one value is zero.
Bitwise XOR	            | Fast	        | Complex	        | Works only with integers.
Tuple Swapping	        | Fast	        |  Very Readable	| Swift-specific and most idiomatic.



