# Typescript Documentation

This is a comprehensive collection of books, courses and repositories designed to provide an essential resource for learning Typescript.  I hope it will be of great help to you!



| Page | Topics  |
|---------------------|--------------|
| 01                   | [Introduction](./README.md)    |
| 02                   | [Interfaces](./01-Interfaces/INTERFACES.md)    |


## Introduction

While working with TypeScript, it is very common to find code as follows:
```ts
let age: number = 20;
   let existsFlag: boolean = true;
   let language: string = 'JavaScript';
```

TypeScript allows us to assign a type to a variable. But the preceding code is verbose. TypeScript has type inference, meaning TypeScript will verify and apply a type to the variable automatically based on the value that was assigned to it. Let's rewrite the preceding code with a cleaner syntax

```ts
let age = 20; // number
   let existsFlag = true; // boolean
   let language = 'JavaScript'; // string
```

With the preceding code, TypeScript still knows that age is a number, existsFlag is a boolean, and language is a string, so we don't need to explicitly assign a type to these variables.

So, when do we type a variable? If we declare the variable and do not initialize it with a value, then it is recommended to assign a type, as demonstrated by the following code:

```ts
   let favoriteLanguage: string;
   let langs = ['JavaScript', 'Ruby', 'Python'];
   favoriteLanguage = langs[0];
```

If we do not type a variable, then it is automatically typed as any, meaning it can receive any value, as it is in JavaScript.


### Other TypeScript Functionalities
This was a very quick introduction to TypeScript. The TypeScript documentation is a great place for learning all the other functionalities and to dive into the details of the topics we quickly covered in this chapter; it can be found at https://www.typescriptlang.org/docs/

