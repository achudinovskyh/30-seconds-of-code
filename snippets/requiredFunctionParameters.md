---
title: requiredFunctionParameters
tags: function,intermediate
---

Creates a function that will ensure that a required parameter has been provided to the function.

- Set `required` function call as a default value for the parameter that is needed to be required.
- If `greet` is called without the required `name` parameter, an error will be thrown.

```js
const required = (name) =>
  { throw new Error(`${name} parameter is required`) };

const greet = (name = required('name')) =>
  console.log(`Hello ${name}!`);
```

```js
greet('Max'); // Hello Max!
greet() // Error: name parameter is required
```
