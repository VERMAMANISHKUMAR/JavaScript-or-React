# JavaScript Data Types & Operators

## Data Types:

**Primitive Data Types:**

- Number: integers, floats, etc.
- String: text data.
- Boolean: true or false.
- Null: represents intentional absence of any object value.
- Undefined: represents a variable that has not been assigned a  value.

**Non-primitive Data Types:**

- Object: a collection of key-value pairs.

- Function: a reusable block of code.

- Array: a collection of elements.

***************************************************************

### 3. Arithmetic Operators:

+ Addition (+)
+ Subtraction (-)
+ Multiplication (*)
+ Division (/)
+ Modulus (%)
+ Increment (++)
+ Decrement (--)

### 4. Assignment Operators:
+ Assignment (=)
+ Addition Assignment (+=)
+ Subtraction Assignment (-=)
+ Multiplication Assignment (*=)
+ Division Assignment (/=)

### 5. Comparison Operators:

+ Equal to (==)
+ Not equal to (!=)
+ Strict equal to (===)
+ Strict not equal to (!==)
+ Greater than (>)
+ Less than (<)
+ Greater than or equal to (>=)
+ Less than or equal to (<=)

### 6. Logical Operators:


+ Logical AND (&&)
+ Logical OR (||)
+ Logical NOT (!)

### 7. Bitwise Operators:
+ Bitwise AND (&)
+ Bitwise OR (|)
+ Bitwise XOR (^)
+ Bitwise NOT (~)
+ Left Shift (<<)
+ Right Shift (>>)
+ Zero-fill Right Shift (>>>)

### 8. Unary Operators:
**Unary operators are used to perform operations on a single operand.**
+ typeof
+ delete
+ new
+ void
**Sure! Here are code examples for each type of operator along with explanations:**

**Arithmetic Operators:**
```// Addition
let resultAdd = 5 + 3; // resultAdd will be 8

// Subtraction
let resultSub = 10 - 4; // resultSub will be 6

// Multiplication
let resultMul = 6 * 2; // resultMul will be 12

// Division
let resultDiv = 20 / 5; // resultDiv will be 4

// Modulus (Remainder)
let resultMod = 10 % 3; // resultMod will be 1

// Increment
let count = 5;
count++; // Increment count by 1, now count is 6

// Decrement
let value = 8;
value--; // Decrement value by 1, now value is 7
Assignment Operators:
let x = 10;
x += 5; // Equivalent to: x = x + 5, so x will be 15

let y = 20;
y -= 3; // Equivalent to: y = y - 3, so y will be 17

let z = 4;
z *= 2; // Equivalent to: z = z * 2, so z will be 8

let w = 15;
w /= 3; // Equivalent to: w = w / 3, so w will be 5
Comparison Operators:
let a = 5;
let b = 10;

// Equal to
console.log(a == 5); // true

// Not equal to
console.log(b != 10); // false

// Strict equal to (compares both value and type)
console.log(a === '5'); // false

// Strict not equal to
console.log(b !== '10'); // true

// Greater than
console.log(a > 3); // true

// Less than
console.log(b < 15); // true

// Greater than or equal to
console.log(a >= 5); // true

// Less than or equal to
console.log(b <= 10); // true
Logical Operators:
let p = true;
let q = false;


// Logical AND

console.log(p && q); // false

// Logical OR
console.log(p || q); // true

// Logical NOT
console.log(!p); // false
Bitwise Operators:
let num1 = 5; // binary: 101
let num2 = 3; // binary: 011

// Bitwise AND
console.log(num1 & num2); // 1 (binary: 001)

// Bitwise OR
console.log(num1 | num2); // 7 (binary: 111)

// Bitwise XOR
console.log(num1 ^ num2); // 6 (binary: 110)

// Bitwise NOT (Unary)
console.log(~num1); // -6

// Left Shift
console.log(num1 << 1); // 10 (binary: 1010)

// Right Shift
console.log(num1 >> 1); // 2 (binary: 10)

// Zero-fill Right Shift
console.log(num1 >>> 1); // 2 (binary: 10)
Unary Operators:
let value = 10;

// typeof operator
console.log(typeof value); // "number"

// delete operator
let obj = { x: 5, y: 10 };
delete obj.x; // Deletes property 'x' from obj

// new operator
function Person(name) {
  this.name = name;
}
let person = new Person('John');

// void operator
let result = void 0; // result is undefined```