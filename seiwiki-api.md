## SEIWIKI-API
 ```
 //schema.sql
 -- always single quote in sql ' '
CREATE DATABASE seiwiki;

CREATE TABLE bookmarks (
  id SERIAL PRIMARY KEY,
  url TEXT NOT NULL,
  description TEXT
);
INSERT INTO bookmarks (description, url) VALUES ('fun way to learn sql', 'https://sqlbolt.com/');


//server.js
const express = require("express");
const pg = require("pg");
// only module come with express
const bodyParser = require("body-parser");
// make new object , Pool is a function or class
// Pool connect to the database
const pool = new pg.Pool({ database: "seiwiki" });

const app = express();
const port = 8080;
// middleware which will parse JSON request into objects
app.use(bodyParser.json());

//read
app.get("/", (req, res) => {
  res.json({ welcome: "seiwiki api" });
});

app.get("/bookmarks", (req, res) => {
  pool
    .query("SELECT * FROM bookmarks;")
    .then(results => res.json({ data: results.rows }));
});

// create
app.post("/bookmarks", (req, res) => {
  // req.query-data was send via querystring
  // req.params - data was send via pretty URLSearchParams
  // req.body- data send via FormData or urlencoded
  // data send via json - wont work with sinatra
  // SELECT->RETURNING * NEW RECORD->SHOW ON JSON,
  pool
    .query(
      "INSERT INTO bookmarks(url, description) VALUES ($1, $2) RETURNING *;",
      [req.body.url, req.body.description]
    )
    // async so put then to finish first
    .then(results => {
      res.json({ results: results.rows });
    });
});

app.listen(port, () => {
  console.log(`seiwiki api listening on ${port}`);
});

 ```
