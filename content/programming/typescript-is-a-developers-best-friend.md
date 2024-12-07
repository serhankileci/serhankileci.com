---
title: "typescript is a developer's best friend"
date: 2024-11-24T18:26:36+03:00
draft: true
---

**What**

...

**Why**

...
Use an <p class="tooltip" data-title="integrated development environment">IDE</p> with a TypeScript language server extension for the best <p class="tooltip" data-title="foobar">DX</p>. The language server will infer the types as you write and intellisense will suggest the relevant types for you.

```ts
const a: string = "foobarbaz";
const b: number = 5;
const c: boolean = true;
````

TypeScript can infer most basic types, so you don't have to explicitly set the type of every variable. The rule of thumb is to enforce a specific type, even if you know the variable with a string value will be inferred as a string type and that you will not change it later, i.e. a function that must return an array, even if the return itself is of an array type.

### Type narrowing

In order for TypeScript to understand a set that can be multiple types, but at some point we want it to know exactly which type we want it to suggest to us and refrain from type errors, there are many ways to go about it. Type narrowing is one.

```ts
function example(x: string | number): void {
 if (x)
}

Basically, we give TypeScript a way to know, under these conditions, this data can only be *this* specific type.

### Generics

A generic is a type argument, like a function argument, but for types that ask for arguments.

```ts
type Foo<Type extends string | number> = Type extends string ? `__${Type}` : 10 + Type;

const bar: Foo<"baz"> = "" // TypeScript will suggest "__baz"
