# interview
test
Interview Questions Java script 

What is hoisting in JavaScript?

How does hoisting work with var and let/const and are you using var in the code ?

Slice and splice ?
Foreach, for in , for of  ?



var: Hoisted with undefined initialization.
let: Hoisted to the top of the block scope, but not initialized

Question1:
console.log(a);
var a = 10;

Answer:  // undefined

Question2:
console.log(b); 
let b = 20;

Answer: // ReferenceError: Cannot access 'b' before initialization

What is the "temporal dead zone" (TDZ)?

The TDZ refers to the time between the start of a block and the point where a let or const variable is declared and initialized. During this period, the variable is in a "dead zone" where it cannot be accessed. Accessing it will result in a ReferenceError.

Question:
{
  console.log(z); 
  let z = 30;
}

Answer - // ReferenceError: Cannot access 'z' before initialization

How does hoisting affect function expressions?


Question:
console.log(myFunc); 
console.log(myFunc());

var myFunc = function() {
  return "Hello, world!";
};

Answer:
// undefined
 // TypeError: myFunc is not a function

How does hoisting work with class declarations?
Class declarations are hoisted to the top of their block scope but are not initialized. Similar to let and const, accessing a class before its declaration results in a ReferenceError.

const myInstance = new MyClass(); // ReferenceError: Cannot access 'MyClass' before initialization

class MyClass {
  constructor() {
    console.log('Class instantiated!');
  }
}

Explain the hoisting behavior in an IIFE (Immediately Invoked Function Expression)
An IIFE is a function expression that is executed immediately after its creation. Variables declared within an IIFE are hoisted to the top of the IIFE's scope, not the global scope.

(function() {
  console.log(a); // undefined
  var a = 10;
})();

console.log(a); // ReferenceError: a is not defined



Question should ask

Question1
console.log(a); // undefined
console.log(b); // ReferenceError: Cannot access 'b' before initialization
console.log(c); // ReferenceError: Cannot access 'c' before initialization

var a = 1;

function foo() {
  console.log(a); // undefined
  var a = 2;
}

foo();

let b = 3;
const c = 4;

Questions 2 
(function() {
  console.log(a); // undefined
  var a = 10;
})();

console.log(a); // ReferenceError: a is not defined

Question3:
console.log(myFunc); 
console.log(myFunc());

var myFunc = function() {
  return "Hello, world!";
};

Answer:
// undefined
 // TypeError: myFunc is not a function

What is the difference between == and === operators ?

What is the difference between let, var and const in Javascript ?

Null , undefined ?

Filter, Map, Reducer ?

shallow Copy and deep copy

Spred Operator ,

Question:
let original1 = {a: 1, b:{c: 4}};
let deepCopy = JSON.parse(JSON.stringify(original1));
deepCopy.b.c = 10;

Question:

let original = {a: 1, b:{c: 4}};
let shallowCopy = Object.assign({}, original);
shallowCopy.b.c = 8;
console.log('original object', original.b.c);





TypeScript 
https://codewithpawan.medium.com/typescript-interview-questions-intermediate-level-part-2-34d6657bc4d7
What is the difference between interface and type in TypeScript?
What is the any type, and why is it generally avoided?
What are TypeScript decorators and how are they used?
unknown
unknown is a type introduced in TypeScript (and not a JavaScript type) to represent values that could be anything, and its use is specifically for TypeScript's type system

What are mapped types in TypeScript?
What are TypeScript decorators and how are they used?
How do you use the keyof and typeof operators in TypeScript?


What are modules in TypeScript and how do they work?


How does TypeScript’s type inference work?


How do you work with advanced types like Partial, Pick, and Omit in TypeScript?

How do you handle asynchronous operations in TypeScript?

How do you define and use utility types in TypeScript?



React Native 
https://www.turing.com/interview-questions/react-native
 Expo/ Native CLI for React Native development.
Explain the Virtual DOM and its relevance in React Native.

Explain the architecture of a React Native app.
List the essential components of React Native
How many threads run in React Native?

How do you handle platform-specific code in React Native?

How would you style a React Native component?

What is 'state' in React Native and how is it different from 'props'?
How would you debug a React Native application?
How do you handle navigation between screens in React Native?
What are 'keys' in React Native and why are they important in lists?
Describe the purpose of 'AsyncStorage' in React Native.
How can you make a network request in React Native?
How do you optimize performance in a React Native application?
Explain the concept of 'HOC' (higher-order component) in React Native.
How can you integrate third-party libraries in a React Native app?

Explain the concept of 'Babel' and its role in React Native development.

Push notifications?
SafeareaView/Fatlist/map/scrollview / touchable opacity 


HOW are handling crashes in the application?
React JS
React Memo, Usecallback ?
HOC?
uselayoutEffect?
How to handle asynchronous operations in javascript ?


Redux-SAGA/RTX
How are are manning state in your application ?
COntext API?
Redux SAGA?
Redux tool KIT?


How are managing security in the react native app?
HOw are you handling crashes in react native app?
HOw are you people release builds to testers ?
How are debugging  react native app?
SOLID principles ?


