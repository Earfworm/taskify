#React TypeScript tutorial

-//react typeScript docs
https://create-react-app.dev/docs/adding-typescript/

-This tutorial is helping me refresh on
typescript react.

https://www.youtube.com/watch?v=FJDVKeh7RJI

-tutorial created by roadsidecode on freeCodeCamp youtube page.

## TypeScript Basics

let name: string;
let age: number | string; //| is called a union gives type options
let isStudent: boolean;
let hobbies: string[]; // string array
let role: [number, string]; /_must match the type is called a tuple_/

//two ways to define a function
let printName: Function;
let printName2: (name: string) => void; //the return type can be a datatype or void if nothing is returned
let printName3: (name: string) => never; //void returns undefined never returns nothing
//instead of - any use - unknown
let personName4: unknown;
// type Person = {
// name: string;
// age?: number; //? makes property optional
// };
// let person: Person = {
// name: "DeShawn",
// };
// console.log(person);

// let lotsOfPeople: Person[] = [
// { name: "Reid", age: 35 },
// { name: "Angela", age: 33 },
// ];

//aliases are type and interface

interface Person {
name: string;
age?: number;
}

//extending interface
interface Guy extends Person {
profession: string;
}

//extending types (adding types together with type &)
type X = {
a: string;
b: number;
};
type Y = X & {
c: string;
d: number;
};

let y: Y = {
c: "string",
d: 4,
a: "string",
b: 3,
};

//extending type with interfaces
type Z = Person & {
a: string;
b: number;
};

//extending interfaces
interface Person2 extends X {
name: string;
age?: number;
}
