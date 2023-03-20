Chapter 1: Introduction to TypeScript (Duration: 30 minutes)

1.1. What is TypeScript?

TypeScript is a statically-typed superset of JavaScript that adds optional type annotations to the language. Developed and maintained by Microsoft, TypeScript aims to provide better tooling, maintainability, and scalability for large-scale JavaScript applications. Since TypeScript is a superset of JavaScript, valid JavaScript code is also valid TypeScript code. TypeScript compiles down to JavaScript, which means it can run on any platform that supports JavaScript.

1.2. Why TypeScript?

Type Safety: TypeScript provides optional static typing, which helps to catch type-related errors during development and not at runtime.
Enhanced Tooling: TypeScript's type system enables better code completion, refactoring, and type checking in popular editors like Visual Studio Code.
Better maintainability and scalability: TypeScript's features like classes, interfaces, and namespaces make it easier to write and manage large-scale applications.
Easier collaboration: TypeScript's type system helps to document and communicate the expected behavior of a piece of code, making it easier for teams to work together.
Compatibility: TypeScript supports ECMAScript features from past, present, and future, making it easy to transition between different versions of JavaScript.
1.3. TypeScript vs. JavaScript

TypeScript is a superset of JavaScript, meaning all valid JavaScript code is also valid TypeScript code.
TypeScript introduces static typing, while JavaScript is dynamically typed.
TypeScript has support for interfaces, namespaces, and decorators, while JavaScript does not.
TypeScript code needs to be transpiled to JavaScript before running on browsers or Node.js, while JavaScript code can run directly.
TypeScript provides better tooling and type checking compared to JavaScript.
In this chapter, we introduced TypeScript, its benefits, and how it compares to JavaScript. In the next chapter, we will set up TypeScript and learn how to configure it.




Mohit Talniya
Give example of each
Here are examples for each topic discussed in Chapter 1.

1.1. What is TypeScript?

JavaScript code (valid TypeScript code):

javascript
Copy code
function greet(name) {
  return `Hello, ${name}!`;
}

console.log(greet("World"));
TypeScript code:

typescript
Copy code
function greet(name: string): string {
  return `Hello, ${name}!`;
}

console.log(greet("World"));
1.2. Why TypeScript?

Type Safety example:

typescript
Copy code
function add(a: number, b: number): number {
  return a + b;
}

const sum: number = add(5, 10); // Works fine
const incorrectSum: number = add("5", "10"); // Error: Argument of type 'string' is not assignable to parameter of type 'number'
Enhanced Tooling example:
TypeScript enables better code completion and refactoring in editors like Visual Studio Code. For instance, when you type a period (.) after an object, the editor will show you a list of properties and methods available for that object.

Better maintainability and scalability example:

typescript
Copy code
interface Person {
  firstName: string;
  lastName: string;
}

class Employee implements Person {
  constructor(public firstName: string, public lastName: string, private salary: number) {}

  getFullName(): string {
    return `${this.firstName} ${this.lastName}`;
  }
}

const employee = new Employee("John", "Doe", 50000);
console.log(employee.getFullName());
1.3. TypeScript vs. JavaScript

Static typing in TypeScript:

typescript
Copy code
function greet(name: string): string {
  return `Hello, ${name}!`;
}
Dynamic typing in JavaScript:

javascript
Copy code
function greet(name) {
  return `Hello, ${name}!`;
}
Interfaces in TypeScript:

typescript
Copy code
interface Person {
  firstName: string;
  lastName: string;
}

function greet(person: Person): string {
  return `Hello, ${person.firstName} ${person.lastName}!`;
}

const person = {
  firstName: "John",
  lastName: "Doe",
};

console.log(greet(person));
Namespaces in TypeScript:

typescript
Copy code
namespace Animals {
  export class Dog {
    constructor(public name: string) {}

    bark(): string {
      return `${this.name} says woof!`;
    }
  }

  export class Cat {
    constructor(public name: string) {}

    meow(): string {
      return `${this.name} says meow!`;
    }
  }
}

const dog = new Animals.Dog("Buddy");
console.log(dog.bark());

const cat = new Animals.Cat("Whiskers");
console.log(cat.meow());
Decorators in TypeScript:

typescript
Copy code
function logClass(target: Function) {
  console.log(`Class ${target.name} has been created.`);
}

@logClass
class Person {
  constructor(public firstName: string, public lastName: string) {}
}

const person = new Person("John", "Doe");