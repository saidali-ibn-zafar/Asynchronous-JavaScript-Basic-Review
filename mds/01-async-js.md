# What is Async JavaScript?

- In a very simplistic nutshell asynchronous code is code that can start now finish later.

![image](https://github.com/saidali-ibn-zafar/Asynchronous-JavaScript-Basic-Review/assets/120341849/dec35754-191d-4ffa-81ce-763fc5468022)

- - - - -

JavaScript by its very nature is a synchronous language and that basically means that JavaScript can excute only one statement at a time from top to bottom...

```js
console.log("line one"); // runs first 
console.log("line two"); // runs second 
console.log("line three"); // runs third 
```

- - - - -

```js
console.log(1);
console.log(2);

setTimeout(() => {
  console.log('callback function fired');
}, 2000);

console.log(3);
console.log(4);

// output:
//  1
//  2
//  3
//  4
//  {after 2000ms} callback function fired

```


- - - - - 

# single-threaded language

- Javascript is a single-threaded language, meaning that just one line of code may be run at once.

