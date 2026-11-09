🔑 var, let & const

This is my practice work on the three keywords used to create variables in JavaScript: var, let and const.

I wrote 5 examples for each keyword, ran them in the browser console, and compared how they behave. The goal was to understand the differences, not only memorise them.

🗂️ Folder Structure
📁 var, const, let
 ├── index.html    → links all three scripts
 ├── var.js        → 5 examples with var
 ├── let.js        → 5 examples with let
 └── const.js      → 5 examples with const
⚖️ Side-by-Side Comparison
	var	let	const
Reassign the value	✅	✅	❌
Declare the same name again	✅	❌	❌
Scope	Function	Block	Block
Best used for	Older code	Values that change	Values that stay fixed
🟠 var

The original way to declare a variable. It is flexible, but that flexibility can cause bugs.

js
// Redeclaring the same name is allowed
var city = "Islamabad";
var city = "Lahore";
console.log(city);  // Lahore

// Joining strings into one
var firstName = "Hajra";
var lastName = "Syed";
var fullName = firstName + " " + lastName;
console.log(fullName);  // Hajra Syed

// A var inside a function stays inside that function
function greet() {
  var greeting = "Asalamu Alaikum! This is Hajra.";
  console.log(greeting);
}
greet();

// Simple maths
var a = 5;
var b = 10;
var sum = a + b;
console.log(sum);  // 15
🟢 let

Used for values that will change later. It only exists inside the block where it is declared, which makes it safer than var.

The let examples are in let.js.

🔴 const

Used for values that should never be reassigned.

js
const pi = 3.14;
console.log(pi);  // 3.14

const country = "Pakistan";
console.log("I live in " + country);  // I live in Pakistan

const price = 500;
const quantity = 3;
const total = price * quantity;
console.log(total);  // 1500

Surprising part: a const array or object can still change on the inside. Only the variable itself can't point to something new.

js
const fruits = ["apple"];
fruits.push("banana");
console.log(fruits);  // ["apple", "banana"]

const student = { name: "Ali", age: 18 };
student.age = 19;
console.log(student.age);  // 19
🧠 What I Learned
var allows redeclaring the same name, which can silently overwrite values.
let and const are block-scoped, so they stay where I put them.
const protects the variable, not the contents of an array or object.
A good habit: start with const, and switch to let only when the value needs to change.
▶️ How to Run
Open the folder in VS Code.
Open index.html in your browser (or use Live Server).
Press F12 and open the Console tab to see the output.
<p align="center">Small files, clear concepts. ✨</p>
