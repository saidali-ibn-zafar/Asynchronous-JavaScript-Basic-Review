# HTTP Requests 

- We make HTTPS requests to get data from another server

- We make these requests to API endpoints

- Example API endpoint:
  - [http://www.musicapi.com/artist/moby](http://www.musicapi.com/artist/moby)

  ![image](https://github.com/saidali-ibn-zafar/Asynchronous-JavaScript-Basic-Review/assets/120341849/0c5b773e-3af4-4d5e-8a5a-17e2db4e92df)

- - - - - 

 ![image](https://github.com/saidali-ibn-zafar/Asynchronous-JavaScript-Basic-Review/assets/120341849/9e00aea3-0f0b-4d40-92b7-3ec2c51f84f8)

 ```js
 const request = new XMLHttpRequest();

 request.addEventListener("readystatechange", () => {

 console.log(request, request.readyState);

 });

request.open("GET", "https://jsonplaceholder.typicode.com/todos/");
request.send();

 ```
 ![image](https://github.com/saidali-ibn-zafar/Asynchronous-JavaScript-Basic-Review/assets/120341849/ca7fcac4-1bbd-47be-939b-436b7fd7b7df)


- - - - -
 ```js
 const request = new XMLHttpRequest();

   request.addEventListener("readystatechange", () => {
  //   console.log(request, request.readyState);

  if (request.readyState === 4) {
    console.log(request.responseText);
  }
  });

request.open("GET", "https://jsonplaceholder.typicode.com/todos/");
request.send();

 ```
 ![image](https://github.com/saidali-ibn-zafar/Asynchronous-JavaScript-Basic-Review/assets/120341849/4df2b0a6-485a-483c-9b1c-96e6127b437c)
