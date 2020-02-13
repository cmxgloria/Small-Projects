```
//horse server.js

const express = require("express");
// create an app object
const cors = require("cors");
const app = express();
// enable all crosss origins request, if no ajax or no cors
app.use(cors());
app.get("/", (req, res) => {
  res.json({ welcome: "express api intro" });
});

app.get("/api/horses", (req, res) => {
  var horses = [
    {
      name: "maythehorsebewithu",
      active: true,
      country: "AUS",
      yearOfBirth: 2000,
      hourlyRate: 30,
      numOfHoursWorked: 2000
    },
    {
      name: "my wife knows everthing",
      active: true,
      country: "USA",
      yearOfBirth: 2007,
      hourlyRate: 50,
      numOfHoursWorked: 2500
    },
    {
      name: "arrrrr",
      active: true,
      country: "USA",
      yearOfBirth: 2004,
      hourlyRate: 30,
      numOfHoursWorked: 2000
    },
    {
      name: "hoof hearted",
      active: false,
      country: "AUS",
      yearOfBirth: 1981,
      hourlyRate: 88,
      numOfHoursWorked: 900
    },
    {
      name: "pony",
      active: false,
      country: "AUS",
      yearOfBirth: 2003,
      hourlyRate: 12,
      numOfHoursWorked: 9000
    },
    {
      name: "sunny boy",
      active: true,
      country: "AUS",
      yearOfBirth: 2003,
      hourlyRate: 42,
      numOfHoursWorked: 6450
    }
  ];
  res.json(horses);
});
app.listen(8080, () => {
  console.log("api listening on port 8080");
});
```

horse clientside app.js
```
// talk to api and get information then show on the web app
const section = document.querySelector("section");
// maybe we need axios to make http request
const url = "http://localhost:8080/api/horses";
// axios.get(url).then(res => {
//   // for dom- we have dom api or jquery
//   console.log(res.data);
// });
// lodash is for utility functions

axios.get(url).then(res => {
  console.log(res);
  // for dom- we have dom api or jquery
  res.data.forEach(horse => {
    const elem = document.createElement("h2");
    elem.textContent = horse.name;
    section.appendChild(elem);
  });
});



index.html
file:///Users/gloriachen/sei/code-alongs/08-node/horses-client/index.html
show on the browser

horses client
maythehorsebewithu
my wife knows everthing
arrrrr
hoof hearted
pony
sunny boy
```
