# Promise

```js
const getSomething = () =>{
  return new Promise((resolve, reject) => {
    // fetch something
    //resolve("some data");
    reject("some error");
  });
  
};
```
```js
getSomething().then((data) => {
  console.log(data);
}, (err) => {
  console.log(err);
})

getSomething().then((data) => {
  console.log(data);
}).catch(err => {
  console.log(err);
})
```

- - - - - 
```js
const getTodos = (resource) => {

  return new Promise((resolve, reject) =>{
    const request = new XMLHttpRequest();

    request.addEventListener('readystatechange', () => {
      if(request.readyState === 4 && request.status === 200){
        const data = JSON.parse(request.responseText);
        resolve(data);
      } else if (request.readyState === 4){
      reject("error getting resourse");
      }
    });

    request.open("GET", resource);
    request.send();
  });
};

getTodos("todos/luigi.json").then(data => {
  console.log("promise resolved:", data);
}).catch((err) => {
  cosole.log("promise rejected:", err);
})

```js
