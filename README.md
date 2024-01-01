# Javascript-Programming

link of the page : https://workat.tech/ide/online-javascript-compiler


JavaScript Reference & Snippets
Hello World!
console.log("Hello World!");
console.log examples
console.log(100); //100
console.log(3.14); //3.14
console.log(); //Empty Line
Operators
Arithmetic Operators
Addition: +
Subtraction: -
Multiplication: *
Division: /
Remainder/Modulus: %
Relational Operators
Equal To: ==
Greater Than: >
Lesser Than: <
Greater Than or Equal To: >=
Lesser Than or Equal To: <=
Not Equal To: !=
Strict Equal To: ===
Strict Not Equal To: !==
Logical Operators
AND: &&
OR: ||
NOT: !
Assignment Operators
Assign: =
Operate and assign: +=, -=, *=, /=, %=
Increment and Decrement (Post and Pre): ++, --
Variables & Data Types
Unlike typed languages, we do not mention the data type of a variable.

Examples
const num = 42;
const pi = 3.14;
const name = "workat.tech";
As the name const suggests, the variable that we create using const is constant and can't be updated.

Example
const num = 42;
num = 5; //This is invalid
Updating a variable as a very common use case. So how do we do that?

Similar to const, there is another keyword used to create variables: let.

Example
let num = 42;
num = 5; //This is valid
console.log(num); //5
num = num + 1;
console.log(num); //6
Till a few years back (before ES6), there was only one way to create variables and that was using var.

Example
var num = 42;
num = 5;
As mentioned above, const and let were introduced very recently in ES6. Note that it is preferred that we use const and let instead of var. Unlike variables in other languages, variables created using var do not have block scope. Not having block scope can result in unexpected bugs.

We can find the data type of some data using typeof operator.

const num = 42;
console.log(typeof num); //number
console.log(typeof "workat.tech"); //string
JavaScript has the following primitive data types:

string: Any valid string
number: There is no concept of int/float in JS. Every number is a 64-bit floating point number.
boolean: true/false
undefined: This is assigned to variables which have not yet been initialized.
Decision Making and Loops
if...else
if (num === 1) {
    console.log("ONE");
} else if (num === 2) {
    console.log("TWO");
} else if (num === 3) {
    console.log("THREE");
} else {
    console.log("UNKNOWN");
}
switch
switch(num) {
    case 1:
        console.log("ONE");
        break;
    case 2:
        console.log("TWO");
        break;
    case 3:
        console.log("THREE");
        break;
    default:
        console.log("UNKNOWN");
}
while loop
let i = 0;
while (i < 10) {
    console.log(i);
    i++;
}
for loop
for (let i = 0; i < 10; i++) {
    console.log(i);
}
Note that we have used let for creating the iterators in both while loop and for loop as the variable i is getting updated during each iteration.

break, continue
while (true) {
    if (num == 42) {
        break;
    }
    console.log(num);
    num++;
}
while (i < 100) {
    if (i%2 == 0) {
        continue;
    }
    console.log(i);
    i++;
}
Functions
A function can be declared using this format:

function functionName (argument1, argument2, ...) {
    // function body with it's logic
}
Note that since JS is dynamically-typed, we do not need to mention the return type. We instead just mention function. The arguments also do not require a type and should be mentioned directly.

Example
function add (firstNum, secondNum) {
    return firstNum + secondNum;
}

console.log(add(42, 7));
const sum = add(3.14, 2.18);
console.log(sum);
Arrays
Arrays in JS are similar to arrays in other languages. Let's look at how it is declared and initialized:

const nums = [1, 2, 3, 4];
const names = ['Elon Musk', 'Bill Gates', 'Steve Jobs'];
const isPresent = [true, true, false];
Accessing and updating the array elements is also similar to other languages:

console.log(names[0]); //Elon Musk

isPresent[1] = false;
We can get the length of the array through the length property of the array like this:

console.log(names.length);
We can iterate the array similar to other languages:

for (let i = 0; i < names.length; i++) {
    console.log(names[i]);
}
We can also print the array directly by putting it inside console.log:

console.log(nums); //[1, 2, 3, 4]
New elements can be pushed using the push method.

nums.push(5);
console.log(nums); //[1, 2, 3, 4, 5]
The last element can be popped using the pop method.

nums.pop();
console.log(nums); //[1, 2, 3, 4]
The array can be converted to a string using the join method with the parameter acting as the delimiter. Default delimiter is ','.

console.log(nums.join()); //1,2,3,4
console.log(nums.join(' ')); //1 2 3 4
console.log(nums.join(', ')); //1, 2, 3, 4
console.log(nums.join('	')); //1	2	3	4
Objects
To store any non-primitive data, we have objects in JavaScript. In fact, JavaScript is all about objects. Arrays are objects. Any kind of data structure that we need to create can be done through objects. Even functions in JavaScript are objects. Let's look at a few examples of objects:

const course = {
    name: 'Introduction to JavaScript',
    website: 'workat.tech',
    isPaid: true,
    cost: 999
};
The object contains keys and values corresponding to each key. In the above example the keys are name, website, isPaid and cost whereas the values are 'Introduction to JavaScript', 'workat.tech', true and 999.

The key needs to be a string whereas the value can be any primitive data or another object (object, array, functions).
