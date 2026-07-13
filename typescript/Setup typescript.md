
# Check if Node is installed
```sh
node -v
npm -v
```

# Initialize a TypeScript Project
```sh
mkdir ts-demo
cd ts-demo
```
Then init TypeScript Project
```sh
npm init -y
```
This creates a `package.json`.
Clean **Node + TypeScript projects** config
```json
{
  "compilerOptions": {
    // JS version to compile to
    "target": "ES2020",
    // Node.js module system
    "module": "commonjs",
    // your TS source folder
    "rootDir": "./src",
    // compiled JS output folder
    "outDir": "./dist",
    // enable strict type checking
    "strict": true,
    // allow import from commonjs modules
    "esModuleInterop": true,
    "forceConsistentCasingInFileNames": true,
    "skipLibCheck": true,
    // optional: useful for debugging
    "sourceMap": true
  }
}
```



# Install TypeScript

```sh
npm install typescript --save-dev
```
- Install **TypeScript**
- Add it to the `devDependencies` section in your `package.json`.

`--save-dev` tells **npm** to install the package as a **development dependency**, not a regular (production) dependency.

## Simple way to think about it
- `dependencies` → your app **needs it to run**
- `devDependencies` → **you need it to build/test** the app

## Key idea (very important)
+ **`devDependencies` are used to CREATE the app**  
+ **dependencies are used to RUN the app**

# Then check typescript version
```sh
npx tsc --version
```

# Optional (for `Node.js` types):
```sh
npm install @types/node --save-dev
```

# ⚠️ Create `tsconfig.json`
>> Be aware about that command some times make a conflict with other configs and cause a hell 🔥 

This configures your TypeScript compiler:
```sh
npx tsc --init
```
You’ll get a `tsconfig.json` For a basic setup


# Compile & Run
Compile TypeScript → JavaScript:
```sh
npx tsc
```
This will generate `dist/index.js`. Run it:
```sh
node dist/index.js
```
Instead of compiling every time, you can install **ts-node** to run TS directly:
```sh
npm install ts-node --save-dev
npx ts-node src/index.ts
```



----
# Quick start

Minimal modern TypeScript + ESLint setup
```sh
npm install --save-dev typescript eslint @typescript-eslint/parser @typescript-eslint/eslint-plugin @types/node
```
- **`typescript`** → TypeScript compiler (`tsc`)
- **`eslint`** → `Linter` 
- **`@typescript-eslint/parser`** → Lets `ESLint` understand TypeScript
- **`@typescript-eslint/eslint-plugin`** → TypeScript lint rules
- **`@types/node`** → `Node.js` type definitions

**The same command but with specific versions**:
```sh
npm install --save-dev \  
typescript@5 \  
eslint@8 \  
@typescript-eslint/parser@8 \  
@typescript-eslint/eslint-plugin@8 \  
@types/node@20
```

You still need configuration files (Create `tsconfig.json`):
```sh
npx tsc --init
```
`tsconfig.json`: 
+ It is the main configuration file for TypeScript.
 It tells the compiler:
+ Which JavaScript version to output
+ Which files to include/exclude
+ Strictness rules (very important for safety)
+ Module system (`CommonJS`, `ESModules`, etc.)

For Code quality + lint rules:
```sh
npx eslint --init
```
Usually creates one of: `eslint.config.js` or `.eslintrc.json`
It starts an **interactive setup wizard** that creates `ESLint` configuration.
You will be asked questions like:
- Do you use TypeScript?
- Do you use React?
- What style do you prefer?
- Where does your code run? (Node/browser)


-----
# Summary

## Step 1 — Initialize project
```sh
npm init -y
```
This creates a **`package.json`** file, which is required for:
- Tracking dependencies
- Saving `devDependencies`
- Defining your project metadata

## Step 2 — Install packages
```sh
npm install --save-dev \
typescript@5 \
eslint@8 \
@typescript-eslint/parser@8 \
@typescript-eslint/eslint-plugin@8 \
@types/node@20
```
This installs:
- TypeScript
- `ESLint`
- Node type definitions
and saves them into `devDependencies`.
