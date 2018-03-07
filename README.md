Shared configurations for Javascript and Typescript development environments.
Linters, code formatters, compilers, etc.

# Installation

`yarn add git+ssh://git@github.com:FigureWorks/js-ts-resources.git#master`

# Integration

## Prettier
Create a `.prettierrc.js` file in the root of your project that contains:
```
module.exports = require("js-ts-resources/prettierrc");
```

## TSConfig
Create a `tsconfig.json` file in the root of your project that contains:
```
{
    "extends": "./node_modules/js-ts-resources/tsconfig.base.json",
    "compilerOptions": {
        ...
    }
}
```

Note, there is an open [issue](https://github.com/Microsoft/TypeScript/issues/18865) on the TypeScript project about how to deal with node_modules relative import paths.

## TSLint
Create a `tslint.json` file in the root of your project that contains:
```
{
    "extends": ["js-ts-resources/tslint-base.json", "tslint-config-prettier"],
    "rules": {
        ...
    }
}
```
