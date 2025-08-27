Q1. swap two numbers without temprory variable. 

let a = 10;
let b = 15;

// Using arithmetic operations
a = a + b;  // 25
b = a - b;  // 25 - 15 = 10
a = a - b;  // 25 - 10 = 15

console.log("a =", a, "b =", b); // a=15, b=10

conclusion: 
We swapped two numbers without using a temporary variable by applying arithmetic operations (addition and subtraction). 
After execution, the value of a becomes 15 and the value of b becomes 10. 
This proves that swapping can be done without extra memory by manipulating the values directly.

Q2. find 3 large numbers among give array of numbers.
let arr = [4, 5, 8, 6];

// Bubble Sort (Descending Order)
for (let i = 0; i < arr.length - 1; i++) {
    for (let j = 0; j < arr.length - i - 1; j++) {
        if (arr[j] < arr[j + 1]) {
            // swap
            let temp = arr[j];
            arr[j] = arr[j + 1];
            arr[j + 1] = temp;
        }
    }
}

// Pick first 3
let largest3 = arr.slice(0, 3);

console.log("3 largest numbers:", largest3);

conclusion: 
By using Bubble Sort in descending order, the array was rearranged from largest to smallest. 
Then, by selecting the first three elements, we obtained the three largest numbers.
For the given array [4, 5, 8, 6], the result is [8, 6, 5]. 
This shows that sorting helps in easily finding the top values in a list

Q3. break a whole number into digits like 4562 -> 4,5,6,2
let num = 4562;
let digits = [];

while (num > 0) {
    let digit = num % 10;   // last digit
    digits.push(digit);     // push at end
    num = Math.floor(num / 10);
}

digits.reverse(); // reverse at last
console.log(digits); // [4, 5, 6, 2]

conclusion: 
A number (4562) was taken as input.
Using modulus (% 10), the last digit was extracted in each loop.
Each digit was stored in an array using push().
The number was reduced by dividing it by 10 (using Math.floor) each time.
Finally, the array was reversed to correct the digit order.
Output: [4, 5, 6, 2]
This shows how a whole number can be broken into individual digits.

Q4. scale a matrix
let matrix = [
  [1, 2],
  [3, 4]
];

let scale = 2;
let rows = matrix.length;
let cols = matrix[0].length;

let scaledMatrix = [];

// Loop through rows
for (let i = 0; i < rows; i++) {
    scaledMatrix[i] = []; // create new row
    // Loop through columns
    for (let j = 0; j < cols; j++) {
        scaledMatrix[i][j] = matrix[i][j] * scale;
    }
}

console.log(scaledMatrix);

conclusion: 
A scale value (2) was applied to the matrix.
Each element of the matrix was multiplied by the scale.
A new scaled matrix was created.
Original matrix: [ [1, 2], [3, 4] ]
Scaled matrix: [ [2, 4], [6, 8] ]
Scaling means multiplying every element by a constant factor.

Q5. multiply two matrix
let A = [
  [1, 2],
  [3, 4]
];

let B = [
  [2, 0],
  [1, 2]
];

// Dimensions
let rowsA = A.length;
let colsA = A[0].length;
let rowsB = B.length;
let colsB = B[0].length;

let C = [];

for (let i = 0; i < rowsA; i++) {
    C[i] = [];
    for (let j = 0; j < colsB; j++) {
        C[i][j] = 0;
    }
}

for (let i = 0; i < rowsA; i++) {
    for (let j = 0; j < colsB; j++) {
        for (let k = 0; k < colsA; k++) {
            C[i][j] = C[i][j] + (A[i][k] * B[k][j]);
        }
    }
}

console.log(C);

conclusion: 
Two matrices A and B were taken as input.
A result matrix C was created with proper dimensions.
Each element of C was calculated by multiplying corresponding row elements of A with column elements of B and summing them.
Original matrices:
  A = [[1, 2], [3, 4]]
  B = [[2, 0], [1, 2]]
Result after multiplication:
  C = [[4, 4], [10, 8]]
This shows that matrix multiplication combines rows of the first matrix with columns of the second to form a new matrix.

Q6. create a function tp print elements form multi dimentional array
function printMultiArray(arr) {
    let rows = arr.length;
    for (let i = 0; i < rows; i++) {
        let cols = arr[i].length;
        for (let j = 0; j < cols; j++) {
            console.log(arr[i][j]);
        }
    }
}

// Example usage
let multiArr = [
    [1, 2, 3],
    [4, 5],
    [6, 7, 8, 9]
];

printMultiArray(multiArr);

conclusion: 
A function printMultiArray() was created to handle multi-dimensional arrays.
It uses nested loops:
Outer loop → goes through each row.
Inner loop → prints each element inside the row.
Example array: [[1, 2, 3], [4, 5], [6, 7, 8, 9]]
Output prints all elements one by one in order:

