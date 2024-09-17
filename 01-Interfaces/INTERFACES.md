# JavaScript Documentation
Back to home: [<< Index ](../README.md)

## Interfaces

In TypeScript, there are two concepts for interfaces. The first one is related to assigning a type to a variable. Consider the following code:
```ts
interface Person {
     name: string;
     age: number;
}
   function printName(person: Person) {
     console.log(person.name);
}

```

The first concept for the TypeScript interface is that an interface is a thing. It is a description of the attributes and methods an object must have.

Now, let's try using the printName function:

```ts
   const john = { name: 'John', age: 21 };
   const mary = { name: 'Mary', age: 21, phone: '123-45678' };
   printName(john);
   printName(mary);
```

The preceding code does not have any compilation errors. The variable john has a name and age as expected by the printName function. The variable mary has a name and age, but also has phone information.

So, why does this code work? TypeScript has a concept called Duck Typing. If it looks like a duck, swims like a duck, and quacks like a duck, then it must be a duck! In the example, the variable mary behaves like the Person interface, so it must be a Person. This is a powerful feature of TypeScript.

And after running the tsc command again, we will get the following output in the hello-world.js file:
```ts
function printName(person) {
       console.log(person.name);
   }
   var john = { name: 'John', age: 21 };
   var mary = { name: 'Mary', age: 21, phone: '123-45678' };
```
The preceding code is just plain JavaScript. The code completion and type and error checking are available in compile time only.

The second concept for the TypeScript interface is related to object-oriented programming. This is the same concept as in other object-oriented languages such as Java, C#, Ruby, and so on. An interface is a contract. In this contract, we can define what behavior the classes or interfaces that will implement this contract should have. Consider the ECMAScript standard. ECMAScript is an interface for the JavaScript language. It tells the JavaScript language what functionalities it should have, but each browser might have a different implementation of it.

Consider the following code:
```ts
interface Comparable {
     compareTo(b): number;
}
   class MyObject implements Comparable {
     age: number;
     compareTo(b): number {
       if (this.age === b.age) {
return 0; }
       return this.age > b.age ? 1 : -1;
     }
}
```
The Comparable interface tells the MyObject class that it should implement a method called compareTo that receives an argument. Inside this method, we can code the required logic. In this case, we are comparing two numbers, but we could use a different logic for comparing two strings or even a more complex object with different attributes. This interface behavior does not exist in JavaScript, but it is very helpful when working with sorting algorithms, as an example.










