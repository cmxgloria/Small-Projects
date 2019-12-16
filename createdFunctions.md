## function
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
