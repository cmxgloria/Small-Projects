//html
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Document</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div class="container">
      <div class="box1">Box1</div>
      <div class="box2">Box2</div>
      <div class="box3">Box3</div>
    </div>
    <script src="app.js"></script>
  </body>
</html>

```
//css
```
.container {
  display: flex;
  justify-content: space-around;
  padding: 20px;
  margin: 15px;
}
.box1 {
  display: flex;
  align-items: center;
  width: 100%;
  height: 80px;
  margin: 20px;
  border: 1px solid black;
}
.box2 {
  display: flex;
  align-items: center;
  width: 100%;
  height: 80px;
  margin: 20px;
  border: 1px solid black;
}
.box3 {
  display: flex;
  align-items: center;
  width: 100%;
  height: 80px;
  margin: 20px;
  border: 1px solid black;
}

```
//app.js
```
var box1 = document.querySelector(".box1");
var box2 = document.querySelector(".box2");
var box3 = document.querySelector(".box3");

var allGreen = function() {
  if (
    box1.style.backgroundColor === "red" &&
    box2.style.backgroundColor === "red" &&
    box3.style.backgroundColor === "red"
  ) {
    box1.style.backgroundColor = "green";
    box2.style.backgroundColor = "green";
    box3.style.backgroundColor = "green";
  }
};
var changeColor1 = function() {
  box1.style.backgroundColor = "red";
};
box1.addEventListener("click", changeColor1);
box1.addEventListener("click", allGreen);

var changeColor2 = function() {
  box2.style.backgroundColor = "red";
};
box2.addEventListener("click", changeColor2);
box2.addEventListener("click", allGreen);

var changeColor3 = function() {
  box3.style.backgroundColor = "red";
};
box3.addEventListener("click", changeColor3);
box3.addEventListener("click", allGreen);

```
