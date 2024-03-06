# Async Await

Async function always returns a Promise!!!

```js
const getTodos = async () => {
  // empty 
};

const test = getTodos();
console.log(test);
```

![image](https://github.com/saidali-ibn-zafar/Asynchronous-JavaScript-Basic-Review/assets/120341849/93d0846f-ced5-4d0c-af13-3b5765731361)

- - - - - 

```js
const getTodos = async () => {
  fetch("todos/luigi.json").then(() => {
  }) 
};

getTodos();

```


When we are using `async` and `await` we do not have to write like this `fetch("todos/luigi.json").then(() => {
  })` instead we can do like below: 

```js
const getTodos = async () => {
  const response = await fetch("todos/luigi.json")
  console.log(response);
};
getTodos();

```
- - - - - 

And then look these code: 

```js
const getTodos = async () => {
  const response = await fetch("todos/luigi.json")
  const data = await response.json();
  console.log(data);
};
getTodos();

```

When we call .json(), it reads the response body and attempts to parse it as JSON data. 
JSON = JavaScript Object Notation.

then we will have: 

![image](https://github.com/saidali-ibn-zafar/Asynchronous-JavaScript-Basic-Review/assets/120341849/4be9f82b-31f1-42ed-9d5c-63ee0d897144)

- - - - - 


```js
const getTodos = async () => {
  const response = await fetch("todos/luigi.json")
  const data = await response.json();

  return data
};

console.log(1);
console.log(2);
getTodos()
  .then(data => conosole.log("resolved:", data));
console.log(3);
console.log(4);

```

In JavaScript, async functions do not block the execution of the program.

![image](https://github.com/saidali-ibn-zafar/Asynchronous-JavaScript-Basic-Review/assets/120341849/01eeedd8-2e08-4899-b083-e16ab1ad3334)
