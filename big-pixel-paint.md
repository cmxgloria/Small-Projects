```
//index.html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
      <div class="brush_box"></div>
    <form action=>
      <input type="text">
      <button>Set Color</button>
    </form>
    <form action=>
      <input class="poster" type="text">
      <button class="poster">Movie Poster</button>
    </form>
    <div class="canvas"></div>
    <script
      src="https://code.jquery.com/jquery-3.4.1.js"
      integrity="sha256-WpOohJOqMqqyKL9FccASB9O0KwACQJpFTUBLTYOVvVU="
      crossorigin="anonymous"
    ></script>
    <script src="app.js"></script>
  </body>
</html>

```

```
//app.js
console.log("pixel art");
var form = document.querySelector("form");
var input = document.querySelector("input");
var button = document.querySelector("button");
var canvas = document.querySelector(".canvas");
var brushBox = document.querySelector(".brush-box");

var handleClick = e => {
  e.preventDefault();
  brushBox.style.backgroundColor = input.value;
};
form.addEventListener = ("summit", handleClick);

var handlePaint = e => {
  if (e.target.classList.contains("pixel")) {
    e.target.style.backgroundColor = "green";
  }
};
for (var i = 0; i <= 2000; i++) {
  var elem = document.createElement("div");
  elem.classList.add("pixel");
  // elem.addEventListener("click", handlePaint);     no need to handle each child, go to parent
  canvas.appendChild(elem);
}
// event bubbling
// event delegation ,no need to handle each child, go to parent to host
canvas.addEventListener("click", handlePaint);

```

```
style.css
.brush-box {
  width: 10px;
  height: 10px;
  border: 1px solid black;
}
.pixel {
  width: 10px;
  height: 10px;
  border: 1px solid black;
}
.canvas {
  display: flex;
  flex-wrap: wrap;
  padding: 20px;
}

```
