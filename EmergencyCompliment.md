//server.js
```
const express = require("express");
const app = express();
const axios = require("axios");
const _ = require("lodash");

app.set("views", "./views");
app.set("view engine", "ejs");

const compliments = [
  "Your instructors love you",
  "High five = ^5",
  "Shut up and take my money",
  "It's almost beer o'clock",
  "The Force is strong with you"
];
const backgroundColors = ["#FFBF00", "#0080FF", "#01DF3A", "#FF0080"];

// console.log(process.argv);

app.get("/", (req, res) => {
  var greeting = _.sample(compliments);
  const randomColor = _.sample(backgroundColors);
  res.render("home", {
    greeting: greeting,
    randomColor: randomColor
  });
});

// axios request only use the backend or frontend request API, in this situation , no need
// app.get("/name", (req, res) => {
//   axios.get("/name").then(res => {
//     res.render("name", {
//       greetName: name
//     });
//   });
// });
// https://expressjs.com/en/guide/routing.html
app.get("/:userName", (req, res) => {
  res.send(req.params.userName);
});
app.listen(8080);

```

//home.ejs
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Document</title>
    <link rel="stylesheet" href="../style.css" />
  </head>
  <!-- body inline -->
  <body bgcolor="<%= randomColor %>">
    <form action="/" method="get">
      <button>Emergency Compliments</button>
    </form>
    <h1><%= greeting %></h1>
  </body>
</html>
```

//package.json
```
{
  "name": "emergencycompliment",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "start": "nodemon server.js"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
    "axios": "^0.19.2",
    "ejs": "^3.0.1",
    "express": "^4.17.1",
    "lodash": "^4.17.15",
    "nodemon": "^2.0.2"
  }
}
```
