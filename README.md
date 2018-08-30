# eslint-config
```
npm i -D eslint prettier eslint-config-prettier eslint-plugin-prettier eslint-plugin-import babel-eslint babel-preset-env @cyberskunk/eslint-config
```

- create `.eslintrc`:
```
{
  "root": true,
  "parser": "babel-eslint",
  "extends": [
    "@cyberskunk",
    "@cyberskunk/eslint-config/react",
    "@cyberskunk/eslint-config/node",
    "@cyberskunk/eslint-config/es6",
    "prettier"
  ],
  "plugins": [
    "prettier",
    "import"
  ],
  "rules": {
    "prettier/prettier": [
      "error",
      {
        "printWidth": 100,
        "semi": false,
        "singleQuote": true,
        "trailingComma": "all",
        "bracketSpacing": false
      }
    ],
    "import/no-extraneous-dependencies": [
      "error",
      {
        "devDependencies": true,
        "optionalDependencies": false,
        "peerDependencies": false
      }
    ],
    "import/no-commonjs": "off",
    "import/first": "error",
    "import/order": ["error", { "newlines-between": "always"}],
    "import/newline-after-import": ["error", { "count": 1 }],
  }
}
```
- add `.eslintignore`, e.g.:
```
.idea
node_modules
dist
```
- add `lint` script to the `package.json`: `"lint": "eslint ."`
