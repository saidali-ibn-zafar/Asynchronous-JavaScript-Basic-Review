# fetch api

```js

fetch("todos/luigis.json").then(() => {
  console.log("resolve", response);
  return response.json();
}).then(data => {
  console.log(data);
}).catch((err) => {
  console.log("rejected", err);
})

```

### Steps:
- We are fetching the data;
- taking the response
- returning the response.json() that returns a promise
- tack on dot then to there
- and inside we fire function where we actually have access to that data
- we can also catch an error at the end.
