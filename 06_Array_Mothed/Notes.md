# JavaScript Functions

## 1. Named Function:

```function greet(name) {
    return "Hello, " + name + "!";
}```
-Arguments: name
-Parameters: name

## 2. Anonymous Function:

``let greet = function(name) {
    return "Hello, " + name + "!";
};``
-Arguments: name
-Parameters: name

## 3. Arrow Function:

let greet = (name) => {
    return "Hello, " + name + "!";
};
-Arguments: name
-Parameters: name

## 4. Immediately Invoked Function Expression (IIFE):

(function(name) {
    console.log("Hello, " + name + "!");
})("John");
-Arguments: name
-Parameters: name

## 5.**Function Constructor:**

let greet = new Function("name", "return 'Hello, ' + name + '!'");

console.log(greet("John"));
-Arguments: name
-Parameters: name

## 6. Callback Function:

```function greet(name, callback) {
    return callback(name);
}

function sayHello(name) {
    return "Hello, " + name + "!";
}

console.log(greet("John", sayHello));```

**Questions**

*Calculate Area of a Rectangle: Write a function called calculateRectangleArea that takes two parameters, width and height, and returns the area of a rectangle. Test the function with different values.*

*Temperature Conversion: Write a function called convertToFahrenheit that takes a temperature in Celsius as a parameter and returns the temperature converted to Fahrenheit. Test the function with different temperatures.*

*Check if a Number is Even: Write a function called isEven that takes a number as a parameter and returns true if the number is even, and false otherwise. Test the function with different numbers.*

*Reverse a String: Write a function called reverseString that takes a string as a parameter and returns the reverse of the input string. Test the function with different strings.*

*Find the Maximum Number: Write a function called findMax that takes an array of numbers as a parameter and returns the maximum number in the array. Test the function with different arrays.*

**Answers**

**Calculate Area of a Rectangle:**

```function calculateRectangleArea(width, height) {
    return width * height;
}

//Test the function
console.log(calculateRectangleArea(5, 7)); // Output: 35
Temperature Conversion:

function convertToFahrenheit(celsius) {
    return (celsius * 9 / 5) + 32;
}

//Test the function
console.log(convertToFahrenheit(20)); // Output: 68
Check if a Number is Even:

function isEven(number) {
    return number % 2 === 0;
}

// Test the function
console.log(isEven(6)); // Output: true
console.log(isEven(3)); // Output: false
Reverse a String:

function reverseString(str) {
    return str.split('').reverse().join('');
}

// Test the function
console.log(reverseString('hello')); // Output: 'olleh'
Find the Maximum Number:

function findMax(numbers) {
    return Math.max(...numbers);
}

// Test the function
console.log(findMax([3, 7, 2, 9])); // Output: 9```

**These answers provide the implementation of the functions and demonstrate how to use them with sample inputs.**