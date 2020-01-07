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
    <ul class="checklist">
      <li class="item">the software development process</li>
      <li class="item">can not fix</li>
      <li class="item">crisis of confience</li>
      <li class="item">question your career</li>
      <li class="item">question life</li>
      <li class="item">oh it was a type</li>
    </ul>
    <button>reset</button>
    <script src="app.js"></script>
  </body>
</html>
```

//css
```
.completed {
  text-decoration: line-through;
  background: rgb(231, 110, 110);
}
button {
  display: none;
}

```

//app.js
```
var secondLastItem = document.querySelectorAll(".item")[4];
secondLastItem.addEventListener("click", function() {
  secondLastItem.classList.add("completed");
});

//same way as above
var secondLastItem = document.querySelectorAll(".item")[4];
secondLastItem.addEventListener("click", function(event) {
  event.target.classList.add("completed");
  // event.target equal to secondLastItem
});

//if target all items
var secondLastItem = document.querySelectorAll(".item")[4];
var allItem = document.querySelectorAll(".item");
secondLastItem.addEventListener("click", function(event) {
  event.target.classList.add("completed");
});

//cross any item when we click
var allItems = document.querySelectorAll(".item");

for (var i = 0; i < allItems.length; i++) {
  allItems[i].addEventListener("click", function(event) {
    event.target.classList.add("completed");
  });
}

//cross any item when we click using forEach
var allItems = document.querySelectorAll(".item");
allItems.forEach(function(item) {
  item.addEventListener("click", function(event) {
    event.target.classList.add("completed");
  });
});

//cross all items at a time
//check if all selected
var allItems = document.querySelectorAll(".item");
allItems.forEach(function(item) {
  item.addEventListener("click", function(event) {
    event.target.classList.add("completed");
    if (document.querySelectorAll(".completed").length === 6) {
      console.log("all done");
    }
  });
});
```

```
//exercise
```
document.querySelector('.item').style.backgroundColor = 'lightgrey'
document.querySelector('.item').style.textDecoration = 'line-through'

var firstItem = document.querySelector('.item')
undefined
firstItem
<li class=​"item">​the software development process​</li>​
firstItem.textContent
"the software development process"
firstItem.classList
DOMTokenList ["item", value: "item"]
firstItem.classList.remove('completed')
undefined
firstItem.classList.add('hello')
undefined

document.querySelectorAll('.item')
NodeList(6) [li.item, li.item, li.item, li.item, li.item.completed, li.item]
document.querySelectorAll('.item')[4]
<li class=​"item completed" style=​"text-decoration:​ line-through;​ background-color:​ lightgrey;​">​question life​</li>​

"data-id"(id for specific meaning)
event.target.dataset
event.target.getAttribute
```
