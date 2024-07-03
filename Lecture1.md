# Course Introduction 
This is the second course of Advanced TypeScript offered by the University of Hogeschool Rotterdam. The course is taught by Giuseppe Maggiore.

# Introduction
In the first part of the course, we focused on the practical side of functional programming. In this part, we will delve into the theoretical aspects of functional programming. The theoretical foundation of functional programming originates from lambda calculus and mathematical logic. 
> We will be exploring mathematics in this course.

# Category Theory
## Why do I need to know this?
A significant portion of functional programming is based on category theory. Understanding the fundamental concepts of category theory will help you grasp the principles and applications of functional programming.

## What is Category Theory?
Category theory is a branch of mathematics that deals with objects and the relationships between them.

Category theory emphasizes the connections between different objects. Imagine having various cities (objects) and roads connecting them (arrows/morphisms/transformations). 
Category theory focuses on understanding how to navigate from one city to another by taking multiple roads and uncovering the connections between the cities.

## What is an Object?
Objects are entities or types. For example:
Math objects: Sets `A = {1,2,3}`, `B = {4,5,6}`
Programming objects: numbers, strings, or advanced types
```typescript
const n: number = 5;
const s: string = "hello";
type SS = {name: string, age: number};
const specialtype: SS = {name: "john", age: 25};
```

## What is a Morphism (Arrow/Transformation)?
Morphisms are functions that take an object and return another object.
For example:
Math morphisms: functions `f: A -> B` => `f(x) = x + 1`,
 `g: B -> C` => `g(x) = x * 2`
Programming morphisms: functions, methods, classes
```typescript
const f = (x: number): number => x + 1;
const g: (x: number) => number = x * 2;
```
>Taking an object and returning another object is a morphism.

## What is Composition?
Composition is the process of combining two or more morphisms (functions or arrows) to create a new morphism (function or arrow).
For example:
Math composition: `f: A -> B`, `g: B -> C`, `h = g(f(x))` => `h: A -> C`
Programming composition: 
```typescript
const h = (x: number): number => g(f(x));
// f(x) = x + 1
// g(x) = x * 2
// h(x) = g(f(x)) = (x + 1) * 2
```

## What is Identity?
Identity is a type of morphism that takes an object and returns the same object. For example:

Math identity: `f: A -> A`, `f(x) = x`

Programming identity: 

```typescript
const identity: <T>(randomvalue: T) => T = (x) => x;
// takes any type of object and returns the same object
```

> Identity is a morphism that takes an object and returns the same object.

## What is Associativity?

Associativity is a property of composition. Something is associative if you can change the order of the composition and still get the same result. For example:

Math associativity: `f: A -> B`, `g: B -> C`, `h: C -> D`, `h(g(f(x))) = (h(g))(f(x))`

Programming associativity: 

```typescript
const f1 = (x: number): number => x + 1;
const g1 = (x: number): number => x + 2;
const h1 = (x: number): number => x - 1;
const Composed1 = (x: number): number => h1(g1(f1(x)));
const Composed2 = (x: number): number => (h1(g1))(f1(x));
// the order of the composition is changed but the result is the same
```

## Notes 
Notes of live lesson:   
- Category theory is a branch of mathematics 
- It deals with objects and transformations between objects
- It expresses the properties of objects and transformations 
- Objects are represented by letters (a, b, c, d) as points on a map 
- Arrows are represented by (f, g, h) as connections between points 
- Morphisms are transformations 
- Example: function in theory: 
    - `f: a -> b` (f is a function, a is the input, b is the output)
    - `g: b -> c` 
    - `h: a -> c` 
    - `h = g(f(x))` (h is the composition of g and f)
    - `h = g(f(x)) = a -> b -> c` (same thing as `h = g(f(x))` and `f;g` because two functions are connected to each other)
- Identity 
- Associativity / Association 
- Composition

