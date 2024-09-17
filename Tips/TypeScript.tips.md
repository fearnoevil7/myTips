- ***Typescript compiler reads a typescript file then generates a javascript file for it to run.***

<br>

# How to install typescript as an npm package?
- `npm install typescript --save-dev`

<br>

# How to install typescript as an npm package globally?
- `npm install -g typescript`

<br>

# How to run the TypeScript file?
- `tsc <file>.ts`

<br>

# Command to compile typescript file, run output javascript file, and then delete the outputted javascript file after running it.
- `tsc <file>.ts && node <file>.js && rm <file>.js`

<br>

# How to handle "Object is possibly 'null'" TypeScript compiler error?
- The following code will generate the ***Object is possibly 'null'*** error:
    - `let heroSectionWidth: number = document.getElementById("hero").offsetWidth;`
- The are two ways of handling potentially ***null*** or ***undefined*** values returned by the above statement.
    - `let heroSectionWidth: number = document.getElementById("hero")!.offsetWidth;`
        - The exclamation mark ***(!)*** is a non-null assertion operator.
        - It tells TypeScript that you are certain that neither ***null*** nor ***undefined*** will be returned.
        - If it does, TypeScript will throw a runtime error. This is useful when you know for sure that the element exists.
    - `let heroSectionWidth: number = document.getElementById("hero")?.offsetWidth;`
        - The question mark ***(?)*** is the optional chaining operator.
        - It allows you to safely access properties of potentially null or undefined values without causing an error.
        - If ***null*** or ***undefined*** is returned, the expression will short-circuit and return ***undefined***, without throwing an error.
        - This is useful when you're unsure if the element with the specified ID exists in the DOM, and you want to gracefully handle the case where it doesn't.

<br>

# How to handle "Could not parse linter output due to: Expected value but found invalid token at character 1 output: Error: No ESLint configuration found in... "
- Create a .eslintrc file in the root directory of your TypeScript project with the following contents.

```
{
   "env": {
     "browser": true,
     "node": true
   },
   "globals": {
     "chrome": true
   },
   "rules": {
     "no-console": 0,
     "no-empty": [1, { "allowEmptyCatch": true }]
   },
   "extends": "eslint:recommended"
}
```

# Make sure to set the proper parser for your .eslintrc config file.
- Install the ***typescript-eslint*** package using npm.
    - $ `npm install typescript-eslint`
- Set the ***parser*** to ***typescript-eslint*** inside of your ***.eslintrc*** config file.

{
   "env": {
     "browser": true,
     "node": true
   },
   "globals": {
     "chrome": true
   },
   "rules": {
     "no-console": 0,
     "no-empty": [1, { "allowEmptyCatch": true }]
   },
   "extends": "eslint:recommended",
   `"parser": "@typescript-eslint/parser"`
}

<br>

