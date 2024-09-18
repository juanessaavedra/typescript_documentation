# JavaScript Documentation
Back to home: [<< Index ](../README.md)

## Generics

Another powerful feature of TypeScript that is useful to data structures and algorithms is the generic concept. Let's modify the Comparable interface so that we can define the type of the object the compareTo method should receive as an argument:

```ts
interface Comparable<T> {
     compareTo(b: T): number;
}
```

By passing the T type dynamically to the Comparable interface, between the diamond operator <>, we can specify the argument type of the compareTo function:

```ts
class MyObject implements Comparable<MyObject> {
     age: number;
     compareTo(b: MyObject): number {
       if (this.age === b.age) {
return 0; }
       return this.age > b.age ? 1 : -1;
     }
}
```

This is useful so that we can make sure we are comparing objects of the same type, and by using this functionality, we also get code completion from the editor.



