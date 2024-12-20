# Setting up basic typescript project

### Basic project setup
- add .gitignore
- add src/index.ts

### Saves ts a dev dependency as it's needed for development
- npm i typescript --save-dev

### Initialise the project
- npx tsc -init

The command above uses npx (a tool that allows you to execute any JavaScript package available on the NPM registry without even installing it) to run the command that initializes a TypeScript project.
Running this command creates a new tsconfig.json file, which defines how TypeScript and the tsc compiler should interact (what JavaScript version to produce, what files to compile, what directory to compile files to, amongst others)

### tsconfig.json

See https://www.totaltypescript.com/tsconfig-cheat-sheet for details.

{
  "compilerOptions": {
    /* Base Options: */
    "esModuleInterop": true,
    "skipLibCheck": true,
    "target": "es2022",
    "allowJs": true,
    "resolveJsonModule": true,
    "moduleDetection": "force",
    "isolatedModules": true,
    "verbatimModuleSyntax": true,

    /* Strictness */
    "strict": true,
    "noUncheckedIndexedAccess": true,
    "noImplicitOverride": true,

    /* If transpiling with TypeScript: */
    "module": "NodeNext",
    "outDir": "dist",
    "sourceMap": true,

    /* If your code runs in the DOM: */
    "lib": ["es2022", "dom"],
  },
  "include": ["src"]
}


 "scripts": {
  "dev": "tsc --watch"
}