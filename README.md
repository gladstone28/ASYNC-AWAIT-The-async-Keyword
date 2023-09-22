[This is the link to the lesson](https://www.codecademy.com/courses/learn-intermediate-javascript/lessons/async-await/exercises/async-function)

# ASYNC AWAIT

## The async Keyword

The async keyword is used to write functions that handle asynchronous actions. We wrap our asynchronous logic inside a function prepended with the async keyword. Then, we invoke that function.
```js
async function myFunc() {
  // Function body here
};

myFunc();

```
We’ll be using async function declarations throughout this lesson, but we can also create async function expressions:
```js
const myFunc = async () => {
  // Function body here
};

myFunc();
```

async functions always return a promise. This means we can use traditional promise syntax, like .then() and .catch with our async functions. An async function will return in one of three ways:

- If there’s nothing returned from the function, it will return a promise with a resolved value of undefined.
- If there’s a non-promise value returned from the function, it will return a promise resolved to that value.
- If a promise is returned from the function, it will simply return that promise
```js
async function fivePromise() { 
  return 5;
}

fivePromise()
.then(resolvedValue => {
    console.log(resolvedValue);
  })  // Prints 5
```

In the example above, even though we return 5 inside the function body, what’s actually returned when we invoke fivePromise() is a promise with a resolved value of 5.

Let’s write an async function!

### Instructions

1. We provided a function withConstructor() which takes in a number. If the number is 0, it returns a promise that resolves to the string 'zero'. If the number is not 0, it returns a promise that resolves to the string 'not zero'. Take a moment to understand this function and the code that follows. When you’re ready to run it, type node app.js in to the terminal and press enter.

Checkpoint 2 Passed

2. Write an async function, withAsync() which reproduces the functionality of withConstructor(). Though your function will return a promise, it should not construct the promise using the new keyword. Instead, it should rely on the fact that an async function automatically returns a promise.

When you’re ready, check your work to move on to the next step.

Checkpoint 3 Passed

Hint
Remember that an async function returns a promise with a resolved value equal to the return value of that function. The function:
```js
function nativePromise(){
  return new Promise((resolve, reject) => {
      resolve('yay!');
  })
}
```

Could be written:
```js
async function asyncPromise(){
  return 'yay!';
}
```

3. Now test your code! Uncomment the test code we wrote at the bottom of app.js. In the terminal, type node app.js and press enter to execute the code.

memory jog:

/c/Users/glads/Documents/PROJECTS_JS_CODECADEMY/ASYNC-AWAIT-The-async-Keyword
