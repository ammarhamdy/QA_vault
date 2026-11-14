
https://www.typescriptlang.org/docs/handbook/2/basic-types.html

----

# `tsc`, the TypeScript compiler

```sh
npm install -g typescript
```
This installs the TypeScript Compiler `tsc` globally. You can use `npx` or similar tools if you’d prefer to run `tsc` from a local `node_modules` package instead.

Now let’s move to an empty folder and try writing our first TypeScript program: `hello.ts`:
```
// Greets the world.
console.log("Hello world!");
```

 And now let’s type-check it by running the command `tsc` which was installed for us by the `typescript` package.
 ```sh
 tsc hello.ts
 ```
If we look in our current directory, we’ll see a `hello.js` file next to `hello.ts`.

