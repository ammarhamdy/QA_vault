
https://www.typescriptlang.org/docs/handbook/typescript-from-scratch.html

---

We frequently see the question “Should I learn JavaScript or TypeScript?“.

The answer is that you can’t learn TypeScript without learning JavaScript! TypeScript shares syntax and runtime behavior with JavaScript, so anything you learn about JavaScript is helping you learn TypeScript at the same time.


Roughly speaking, once TypeScript’s compiler is done with checking your code, it _erases_ the types to produce the resulting “compiled” code. 

This means that once your code is compiled, the resulting plain JS code has no type information.


This also means that TypeScript never changes the _behavior_ of your program based on the types it inferred. 

The bottom line is that while you might see type errors during compilation, the type system itself has no bearing on how your program works when it runs.


**Finally, TypeScript doesn’t provide any additional runtime libraries.** 
==Your programs will use the same standard library== (or external libraries) as JavaScript programs, so there’s no additional TypeScript-specific framework to learn.


