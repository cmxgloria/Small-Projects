## small projects

```
//created two buttons to add two numbers together
//html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=<device-width>, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Document</title>
  </head>
  <body class="dark">
    <span class="mode-btn">Dark Mode</span>
    <h1>crappy calculator</h1>
    <input class="number1" type="number" value="number" /> +
    <input class="number2" type="number" value="number" /> =
    <span class="result">?</span>
    <button class="submit-btn">submit</button>
    <script src="app.js"></script>
  </body>
</html>

//app.js
var num1 = document.querySelector(".number1");
var num2 = document.querySelector(".number2");
var span = document.querySelector("span");
var submitBtn = document.querySelector(".submit-btn");
//Event handler
var handleClick = function(e) {
  var result = Number(num1.value) + Number(num2.value);
  //input when print is a string ,need to convert using Number
  span.textContent = result;
};

submitBtn.addEventListener("click", handleClick);

var handleToogle = function() {
  document.body.classList.toogle("dark");
  if (modeBtn.textContent === "dark mode") {
    modeBtn.textContent = "light mode";
  } else {
  }
};
//css
body {
  background-color: white;
}
.dark {
  background-color: black;
  color: white;
}
h1 {
  margin-top: 0;
}
.mode-btn {
  position: fixed;
}

```

```
//bank deposit aim to add current deposit and original balance to total balance
//html
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
    <h1>Bank Total Balance</h1>

    $<input id="deposit" type="number" value="number" />
    <button class="deposit-btn">Deposit</button>
    <div class="total">Total: <span class="balance">0</span></div>
    <script src="app.js"></script>
  </body>
</html>

//app.js
var totalBalance = 0;
var deposit = 0;
var depositBtn = document.querySelector(".deposit-btn");
var balanceElement = document.querySelector(".balance");
var handleClick = function() {
  deposit = Number(document.querySelector("#deposit").value);
  var currentBalance = Number(balanceElement.textContent);
  var newBalance = deposit + currentBalance;
  balanceElement.textContent = newBalance;
};

depositBtn.addEventListener("click", handleClick);

```
```
//find wolf to warn sheep project

var sheep = ["sheep", "sheep", "sheep", "sheep", "sheep", "sheep", "sheep"];
var wolfPos = Math.floor(Math.random() * (sheep.length + 1));
function warn() {
  sheep.splice(wolfPos, 0, "Wolf");
  console.log(sheep);
  var warnSheep = sheep.length - (sheep.indexOf("Wolf") + 1);
  if (warnSheep !== 0) {
    console.log(
      `Oi! Sheep number ${warnSheep}! You are about to be eaten by a wolf!`
    );
  } else {
    console.log("Pls go away and stop eating my sheep");
  }
}
warn();
```

### combine html css javascript

```
// create toilet project using addEventListener to click the button to do sth
//file:///Users/gloriachen/sei/code-alongs/02-web/toilet.js/index.html

//html
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
    <div class="tank">
      <div style="background-color:lightgray;" , class="flush-btn"></div>
    </div>
    <div class="bowl"></div>
    <script src="app.js"></script>
  </body>
</html>

//css

* {
  box-sizing: border-box;
}
/* "*" to apply all element */

body {
  background-color: grey;
}
.tank {
  background-color: white;
  width: 400px;
  height: 200px;
  border-radius: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.bowl {
  transition: all linear 400ms;
  background-color: rgb(71, 131, 71);
  width: 400px;
  height: 400px;
  border-radius: 20% 20% 40% 40%;
  /* topleft topright bottomright bottomleft */
  border: 60px solid white;
  padding: 20px;
  box-shadow: inset 0 0 20px grey;
}
.flush-btn {
  width: 200px;
  height: 100px;
  box-shadow: 0 4px 8px 0 grey;
  cursor: pointer;
  text-align: center;
}

//app.js
var bowl = document.querySelector(".bowl");
var flush1 = document.querySelector(".flush-btn");
var poop = function() {
  window.document.body.children[1].style.backgroundColor = "darkolivegree";
};

var flush = function() {
  window.document.body.children[1].style.backgroundColor = "mintcream";
};
// window.document.body.children[1].addEventListener("click", poop);
// window.document.body.children[0].children[0].addEventListener("click", flush);
bowl.addEventListener("click", poop);
flush1.addEventListener("click", flush);

```

```
//crappy calculation to calculate 2 numbers and submit to get value
file:///Users/gloriachen/sei/code-alongs/02-web/crappy-calculator/index.html

//html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=<device-width>, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Document</title>
  </head>
  <body>
    <h1>crappy calculator</h1>
    <input class="number1" type="number" value="number" /> +
    <input class="number2" type="number" value="number" />
    <span>?</span>
    <button class="submit-btn">submit</button>
    <script src="app.js"></script>
  </body>
</html>

//css
var num1 = document.querySelector(".number1");
var num2 = document.querySelector(".number2");
var span = document.querySelector("span");
var submitBtn = document.querySelector(".submit-btn");
//Event handler
var handleClick = function() {
  var sum = Number(num1.value) + Number(num2.value);
  //input when print is a string ,need to convert using Number
  span.textContent = sum;
};

submitBtn.addEventListener("click", handleClick);

```

timer
```
//created a few function to press button to start, pause and reset
//html
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
    <h1>stop watch</h1>
    <div class="timer">0</div>
    <div class="control"></div>
    <button class="start-btn">start</button>
    <button class="pause-btn">pause</button>
    <button class="reset-btn">reset</button>
    <script src="app.js"></script>
  </body>
</html>

//app.js

var timerDiv = document.querySelector(".timer");
var startBtn = document.querySelector(".start-btn");
var pauseBtn = document.querySelector(".pause-btn");
var resetBtn = document.querySelector(".reset-btn");
var second = 0;
var timerId = null;

var tick = function() {
  second++;
  timerDiv.textContent = second;
};
var handleClick = function() {
  //if press to startBtn, can not press again the start button
  if (timerId !== null) {
    return;
  }
  timerId = setInterval(tick, 1000);
};
// startBtn.addEventListener("click", function() {
//   setInterval(tick, 1000);
// });

var handleClickPause = function() {
  clearInterval(timerId);
  //to make start button to work again after you pause and start again.
  timerId = null;
};
//?
var handleClickReset = function() {
  clearInterval(null);
  timerId = null;
};

startBtn.addEventListener("click", handleClick);
pauseBtn.addEventListener("click", handleClickPause);
resetBtn.addEventListener("click", handleClickReset);

```


## function

```
https://files.slack.com/files-pri/T0351JZQ0-FRG8MSSE7/mornings_warmup

var yearSelect = function() {
  var maxyear = 1950;
  var minYear = 1930;
  var setYear = Math.floor(Math.random()) * (maxyear - minYear) + minYear;
  return setYear;
};
var guessTalk = function(talk) {
  var refTalk = talk.toUpperCase();
  return refTalk === talk ? true : false;
};
var grandmaRes = function() {
  var grandmaTalk = "";
  var sonnyTalk = "Good morning";
  while (sonnyTalk !== "BYE") {
    grandmaTalk = guessTalk(sonnyTalk)
      ? `No, NOT SINCE ${yearSelect}`
      : "HUH?!  SPEAK UP, SONNY!";
    console.log(grandmaTalk);
    if (sonnyTalk == "BYE") {
      console("Bye, sonny");
    }
  }
};
grandmaRes();
```
```
// calculate each array and 3 arrays in total- extension.Having placed a $1 bet on each stroke over par that Bob and Jimbo played per hole calculate his winnings.
var totalScores = function(arr) {
  var total = 0;
  for (var i = 0; i < arr.length; i++) {
    total = total + arr[i];
  }
  return total;
};

var getWinings = function(player, par) {
  var win = 0;
  for (var i = 0; i < par.length; i++) {
    var diff = player[i] - par[i];
    win = win + (diff > 0 ? diff : 0);
  }
  return win;
};

// usage
var bob = [3, 2, 6, 11, 9, 2, 6, 9, 10];
var jimbo = [5, 12, 9, 22, 13, 7, 16, 10, 11];
var fish = [2, 2, 4, 5, 4, 3, 6, 4, 1];
var bobTotal = totalScores(bob);
var jimboTotal = totalScores(jimbo);
var fishTotal = totalScores(fish);
var total = bobTotal + jimboTotal + fishTotal;
console.log(`bob total:  ${bobTotal}`);
console.log(`jimbo total: ${jimboTotal}`);
console.log(`fish total:  ${fishTotal}`);
console.log(`total:  ${total}`);

// bet winngings
var par = [3, 4, 5, 5, 3, 3, 4, 3, 5];
var winningsForBob = getWinings(bob, par);
var winningsForJimbo = getWinings(jimbo, par);
var totalWinings = winningsForBob + winningsForJimbo;
console.log(`winnings: ${totalWinings}`);
```

```
//money tree
function printMoneyTree(rows) {
  for (var i = 1; i <= rows; i++) {
    // 2n+1 $ per row i.e. 1, 3, 5, 7, ...
    var dollarSigns = "$".repeat(2 * i - 1);
    var spacesBefore = " ".repeat(rows - i );
    console.log(spacesBefore + dollarSigns);
  }
}
```
```
//return an array of numbers where each number is the length of the corresponding string

var lengths = function(arr) {
  var result = [];
  for (var i = 0; i < arr.length; i++) {
    result.push(arr[i].length);
  }
  return result;
};
```

```
//product of the first two numbers, raised to the power of the third number
var transmogrifier = function(num1, num2, num3) {
  return Math.pow(num1 * num2, num3);
};
console.log(transmogrifier());
//if pass 5,3,2,output 225
```

```
//a string with the order of the words reversed

function wordReverse(string) {
  var result = string.split(" ");
  return result.reverse().join(" ");
}
wordReverse('we are good friends'), output'friend good are we'
```
```
// find the longest word during the array

function findLongestWord(arr) {
  var longestWord = "";
  for (var i = 0; i < arr.length; i++) {
    if (arr[i].length > longestWord.length) {
      longestWord = arr[i];
    }
  }
  return longestWord;
}
```

```
// how to find total vowels number in a word
var countVowels = function(word) {
  var vowels = ["a", "e", "i", "o", "u", "y"];
  var count = 0;
  for (let i = 0; i < word.length; i++) {
    if (vowels.indexOf(word[i]) !== -1) {
      count = count + 1;
    }
  }
  return count;
};

var result = countVowels("stealing");
console.log(result);
// displays 3


//another way

var word = "stealing";
var vowels = ["a", "e", "i", "o", "u", "y"];
var count = 0;
for (var i = 0; i < word.length; i++) {
  for (var j = 0; j < vowels.length; JSON++) {
    if (vowels[j] === word[i]) {
      console.log("its a vowel");
      count++;
    }
  }
}
```

## loop

```
//multitable of 9
var num = 9;
for (var i = 0; i <= 10; i++) {
  var result = num * i;
  console.log(` ${i} * ${num} = ${result}`);
}
```

```
// multitable 0-10 all print out
for (var i = 0; i <= 10; i++) {
  console.log([i] + " times table");
  console.log("=======");
  for (var j = 1; j <= 10; j++) {
    var res = j * i;
    console.log(` ${i} * ${j} = ${res}`);
  }
}
```

```
// guess number
const randomNumber = Math.floor(Math.random() * 11);
while (true) {
  const userInput = prompt("please guess a number between 0 and 10");
  const guessNum = parseInt(userInput);
  if (guessNum === randomNumber) {
    console.log("Congratulation!");
    break;
  }
}
```
```
// guess number

const number = Math.floor(Math.random() * 10001);

while (true) {
  const userInput = prompt("please guess a number between 0 and 10000");
  const guessNum = parseInt(userInput);
  if (guessNum > number) {
    console.log('"Wrong, guess lower!"');
  } else if (guessNum < number) {
    console.log("Wrong, guess higher!");
  } else {
    console.log("Congratulation!");
    break;
  }
}

```
```
//find the multiple number of 7

for (let i = 1; i <= 200; i++) {
  if (i % 7 == 0) {
    console.log(i);
  }
}

//print out all num multiple of 7 between 1-200
```

```
//find the leap year of the last 10 years

for (let i = 1919; i < 2019; i++) {
  if (i % 4 == 0) {
    console.log(i);
  }
}
// print all leap year between 1919-2019
```

```
for (let i = 101; i <= 200; i = i + 3) {
  if (i % 2 == 1) {
    console.log(i);
  }
}
//101 107 113..197
```

```
var drinkAge = 18;
var userIput = prompt("Please put your age");
var age = parseInt(userIput);
if (age >= drinkAge) {
  console.log("Welcome to the relaxing world!!");
} else {
  console.log("Please go home to watch TV.");
}



function checkAC() {
  var currentTem = Number(prompt("What is current temperature?"));
  var AC = prompt("is the AC working?");
  var desiredTemp = Number(prompt("what temperature would you prefer?"));
  if (AC === "yes" && currentTem > desiredTemp) {
    return "Turn on A/C";
  } else if (AC !== "yes" && currentTem > desiredTemp) {
    return 'Fix the AC, it is hot'
  }else if(AC !== "yes" && currentTem < desiredTemp){
return "Fix the A/C whenever you have the chance... It's cool..."
  }else{
    return 'no problem'
  }
}

var suburb;
do{
suburb = prompt('What suburb do you live?');
if(suburb.trim()!== ''){
  console.log(suburb.trim() + 'is a nice place.');
}
  else{
    alert('You did not say anything');
  }
}
while
  (suburb.trim() === '')
 ```

## function inside the object
```
var favoriteMovie = {
  title: "Puff the Magic Dragon",
  duration: 30,
  stars: ["Puff", "Jackie", "Living Sneezes"],
  printDetails: function() {
    console.log(
      `${this.title} lasts for ${
        this.duration
      } minutes. Stars: ${this.stars.join(", ")}.`
    );
    
  }
};
favoriteMovie.printDetails();
```


```
// find the greater number
var greaterNum = function(num1, num2) {
  if (num1 > num2) {
    return num1;
  } else {
    return num2;
  }
};
var num = greaterNum(10, 5);
console.log(num);
```

```
//say hellWorld in 3 different languages

function helloWorld(param){
  if(param==='en'){
    return 'hello world'
  }else if (param === 'es'){
    return 'salute mondo'
  }else if(param === 'de'){
    return 'hallo welt'
  }else{
    return 'ss'
  }
}

//another way

function helloWorld(code) {
  var table = {
    en: "hello world",
    es: "salute mondo",
    de: "hallo welt"
  };
  return table[code];
}
console.log(helloWorld('en'));

```

```
//assign the grade base on the scores

function assignGrade(numScore) {
  if (numScore > 90) {
    return "A";
  } else if (numScore < 80) {
    return "B";
  } else if (numScore < 70) {
    return "C";
  } else if (numScore < 60) {
    return "D";
  } else {
    return "E";
  }
}
assignGrade(70);
```

```
//join the number and name together
var pluralize = function(number, noun) {
  if (number === 1) {
    return `${number} ${noun}`;
  } else {
    return `${number} ${noun}s`;
  }
};
console.log(pluralize(4, "cat"));
```

```
// sort weekday alphabetically

var days_of_the_week = [
  "Monday",
  "Tuesday",
  "Wednesday",
  "Thursday",
  "Friday",
  "Saturday",
  "Sunday"
];
days_of_the_week.pop("Sunday");
days_of_the_week.unshift("Sunday");
console.log(days_of_the_week);
var newDate = [
  ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
  ["Saturday", "Sunday"]
];
newDate.pop(["Saturday", "Sunday"]);
console.log(newDate);
newDate[0].sort();
console.log(newDate);
```


## function activity

```
//concat two words

var combineWords = function(word1, word2) {
  return word1.concat(word2);
};

var result = combineWords("cake", "pudding");
console.log(result);

//cakepudding
```

```
var calculateAge = function(birthYear, currentYear) {
  var age = currentYear - birthYear;
  return age;
};
var myAge = calculateAge(1983, 2019);

console.log(`I am ${myAge} years old or ${myAge + 1} years old.`);
```
