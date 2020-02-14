```
//index.html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Cat</title>
    <TITLE>Activity - Insert animated GIF to HTML</TITLE>
  </head>
  <body>
    <form action="">
      <input type="text" />
      <button>Search</button>
    </form>
    <div></div>
    <button class="load-more-btn hidden">Load More</button>
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
//app.js ----updated
// var apikey = "PPActQ29mRiBim9iLV63aSyam0o0atZ1k";
// var url = `https://api.giphy.com/v1/gifs/search?api_key=PPActQ29mRiBim9iLV63aSyam0o0atZ1k&q=${title}&limit=10&offset=0&rating=G&lang=en`;
// $.ajax({res}).done( callback_function) request and then the response will be ready in the callback function.

console.log("giphy project");

var form = document.querySelector("form");
var input = document.querySelector("input");
var searchBtn = document.querySelector("button");
var divTag = document.querySelector("div");
var imgTag = document.querySelector("img");
var aTag = document.querySelector("a");

var handleClick = function(e) {
  e.preventDefault();
  var handleImage = function(res) {
    console.log(res.data);
    for (let i = 0; i < res.data.length; i++) {
      var elem = document.createElement("img");
      var imageUrl = res.data[i].images.original.url;
      elem.setAttribute("src", imageUrl);
      divTag.appendChild(elem);
    }
  };
  var title = input.value;
  console.log(title);
  var apikey = "PActQ29mRiBim9iLV63aSyam0o0atZ1k";
  var url = `https://api.giphy.com/v1/gifs/search?api_key=${apikey}&q=${title}&limit=10&offset=0&rating=G&lang=en`;
  var options = { url: url, method: "get" };
  $.ajax(options).done(handleImage);
};
searchBtn.addEventListener("click", handleClick);

var handleMore = function(e) {
  e.preventDefault();
  var loadMore = function(res) {
    console.log(res.data);
    for (let i = 0; i < res.length; i + 10) {
      var elem = document.querySelector("img");
      imageUrl = res.data[i].images.original.url;
      elem.setAttribute("src", imageUrl);
      divTag.appendChild(elem);
      var elem1 = document.querySelector("a");
      imageUrl = res.data[i].images.original.url;
      elem1.setAttribute("href", imageUrl);
      aTag.appendChild(elem1);
    }
  };
  var title = input.value;
  console.log(title);
  var apikey = "PActQ29mRiBim9iLV63aSyam0o0atZ1k";
  var url = `https://api.giphy.com/v1/gifs/search?api_key=${apikey}&q=${title}&limit=10&offset=0&rating=G&lang=en`;
  var moreItems = { url: url, method: "get" };
  $.ajax(moreItems).done(loadMore);
};
aTag.addEventListener("scroll", handleMore);

//return res.data[11].images.original.url;
```


//update app.js
```
// var apikey = "PPActQ29mRiBim9iLV63aSyam0o0atZ1k";
// var url = `https://api.giphy.com/v1/gifs/search?api_key=PPActQ29mRiBim9iLV63aSyam0o0atZ1k&q=${title}&limit=10&offset=0&rating=G&lang=en`;
// $.ajax({res}).done( callback_function) request and then the response will be ready in the callback function.
// var responseReady = false;
// var limitScrollTime = 0;

console.log("giphy project");

var form = document.querySelector("form");
var input = document.querySelector("input");
var searchBtn = document.querySelector("button");
var divTag = document.querySelector("div");
var imgTag = document.querySelector("img");
var loadMoreBtn = document.querySelector(".load-more-btn");

var createImages = function(img) {
  var elem = document.createElement("img");
  var imageUrl = img.images.original.url;
  elem.setAttribute("src", imageUrl);
  divTag.appendChild(elem);
};

var search = function() {
  var handleImage = function(res) {
    console.log(res.data);

    for (let i = 0; i < res.data.length; i++) {
      createImages(res.data[i]);
    }
  };
  var title = input.value;
  console.log(title);
  var apikey = "PActQ29mRiBim9iLV63aSyam0o0atZ1k";
  var offset = 10;
  var url = `https://api.giphy.com/v1/gifs/search?api_key=${apikey}&q=${title}&limit=10&offset=${offset}&rating=G&lang=en`;
  var options = { url: url, method: "get" };
  $.ajax(options).done(handleImage);
};

var handleClick = function(e) {
  e.preventDefault();
  search();
};

var handleMore = function(e) {
  e.preventDefault();
  search();
};

searchBtn.addEventListener("click", handleClick);
loadMoreBtn.addEventListener("click", handleMore);
// window.addEventListener("scroll", handleMoreScroll);

// change offset 10

```
// app.js
```
// var apikey = "PPActQ29mRiBim9iLV63aSyam0o0atZ1k";
// var url = `https://api.giphy.com/v1/gifs/search?api_key=PPActQ29mRiBim9iLV63aSyam0o0atZ1k&q=${title}&limit=10&offset=0&rating=G&lang=en`;
// $.ajax({res}).done( callback_function) request and then the response will be ready in the callback function.
// var responseReady = false;
// var limitScrollTime = 0;

console.log("giphy project");

var form = document.querySelector("form");
var input = document.querySelector("input");
var searchBtn = document.querySelector("button");
var divTag = document.querySelector("div");
var imgTag = document.querySelector("img");
var loadMoreBtn = document.querySelector(".load-more-btn");

var createImages = function(img) {
  var elem = document.createElement("img");
  var imageUrl = img.images.original.url;
  elem.setAttribute("src", imageUrl);
  divTag.appendChild(elem);
};

var handleClick = function(e) {
  e.preventDefault();
  var handleImage = function(res) {
    console.log(res.data);

    for (let i = 0; i < res.data.length; i++) {
      createImages(res.data[i]);
    }
  };
  var title = input.value;
  console.log(title);
  var apikey = "PActQ29mRiBim9iLV63aSyam0o0atZ1k";
  var url = `https://api.giphy.com/v1/gifs/search?api_key=${apikey}&q=${title}&limit=10&offset=0&rating=G&lang=en`;
  var options = { url: url, method: "get" };
  $.ajax(options).done(handleImage);
};

var handleMore = function(e) {
  e.preventDefault();
  var loadMore = function(res) {
    console.log(res.data);
    for (let i = 0; i < res.data.length; i++) {
      createImages(res.data[i]);
    }
  };
  var title = input.value;
  console.log(title);
  var apikey = "PActQ29mRiBim9iLV63aSyam0o0atZ1k";
  var url = `https://api.giphy.com/v1/gifs/search?api_key=${apikey}&q=${title}&limit=10&offset=0&rating=G&lang=en`;
  var moreItems = { url: url, method: "get" };
  $.ajax(moreItems).done(loadMore);
};

searchBtn.addEventListener("click", handleClick);
loadMoreBtn.addEventListener("click", handleMore);
// window.addEventListener("scroll", handleMoreScroll);

// change offset 10
```
