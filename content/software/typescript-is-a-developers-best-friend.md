---
title: "💾 typescript is a developer's best friend"
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

TypeScript can infer most basic types, so you don't have to explicitly set the type of every variable. However, it's a good standard to enforce a specific type, even if you know the variable with a string value will be inferred as a string type and that you will not change it later, i.e. a function that must return an array, even if the return itself is of an array type.
