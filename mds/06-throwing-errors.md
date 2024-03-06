# throwing errors

This md does not include lots of new things, here we are just learning how to throw errors. Look at the code below:

```js
const getTodos = async () => {
  const response = await fetch("todos/luigis.json");

  if(response.status !== 200) {
    throwing new Error("cannot fetch the data");
  }

  const data = await response.json();
  return data;
};

getTodos()
  .then(data => console.log("resolve:", data))
  .catch(err => console.log("rejected:" err.message))
```
- - - - 

These codes we are checking the status of the response, and if it is not 200(kinda success), then we are throwing an error.

```js
 if(response.status !== 200) {
    throwing new Error("cannot fetch the data");
  }
```
