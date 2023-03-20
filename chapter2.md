Chapter 2: Setting Up TypeScript (Duration: 30 minutes)

2.1. Installing TypeScript

To install TypeScript globally on your system, use the following command:

bash
Copy code
npm install -g typescript
This will install the TypeScript compiler (tsc) that you can use to compile your TypeScript files into JavaScript.

2.2. TypeScript Compiler (tsc)

After installing TypeScript, you can use the tsc command to compile TypeScript files. For example, if you have a file named main.ts, you can compile it to JavaScript using the following command:

bash
Copy code
tsc main.ts
This will generate a main.js file, which you can run on any platform that supports JavaScript.

2.3. Basic TypeScript Configuration

You can create a TypeScript configuration file (tsconfig.json) to customize the compiler options and include/exclude files for your project. Here's a basic tsconfig.json file:

json
Copy code
{
  "compilerOptions": {
    "target": "es5",
    "module": "commonjs",
    "strict": true,
    "esModuleInterop": true,
    "outDir": "./dist"
  },
  "include": ["src/**/*"],
  "exclude": ["node_modules", "dist"]
}
In this configuration:

target: Specifies the ECMAScript target version. In this case, we target ES5.
module: Specifies the module system to use. In this case, we use CommonJS.
strict: Enables strict type-checking options.
esModuleInterop: Enables CommonJS/AMD module imports.
outDir: Specifies the output directory for the compiled JavaScript files.
include: Specifies the files or folders to include in the compilation process.
exclude: Specifies the files or folders to exclude from the compilation process.
You can customize these options according to your project's requirements. For more options and details, you can refer to the official TypeScript documentation.

In this chapter, we learned how to set up TypeScript, use the TypeScript compiler, and create a basic TypeScript configuration file. 