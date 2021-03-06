```
//html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Tic Tac Toe</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <h1>Tic-Tac-Toe</h1>
    <h2>It's X's turn!</h2>
    <div class="flex-container">
      <div class="flex-container flex-wrap" id="board">
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
      </div>
      <button id="reset-button">reset</button>
    </div>
    <script src="app.js"></script>
  </body>
</html>
```

```
//css
body {
  text-align: center;
}
h1 {
  border: 2px solid salmon;
  background-color: aquamarine;
}
h2 {
  margin: 0 auto;
  font-size: 30px;
  margin: 15px;
  background-color: lightgrey;
}

.flex-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.flex-wrap {
  flex-wrap: wrap;
  /* each square lenght + 2*board */
  height: 462px;
  width: 462px;
}

.square {
  border: 2px solid rgba(0, 0, 0, 0.75);
  height: 150px;
  width: 150px;
  font-size: 80px;
  display: flex;
  align-items: center;
  justify-content: center;
}

#reset-button {
  text-align: center;
  font-size: 30px;
  font: bold;
  border: 1px solid darkgrey;
  background-color: antiquewhite;
  height: 65px;
  width: 120px;
  margin: 20px;
}
```

```
//app.js
// handleTurn function , X and O render, render() to see who win, Win logic,
// 3 (rows) + 3 (columns) + 2 (diagonals) = 8 possible ways to win

let turn = "X";
let board = null;
let win = null;
const winGame = [
  [0, 1, 2],
  [3, 4, 5],
  [6, 7, 8],
  [0, 3, 6],
  [1, 4, 7],
  [2, 5, 8],
  [0, 4, 8],
  [2, 4, 6]
];
// find all 9 boards div children in squares
const squares = Array.from(document.querySelectorAll("#board div"));
const messages = document.querySelector("h2");

//  handleTurn() function to call getWinner() and assign its output to the win variable
function handleTurn(event) {
  // find index of square in squares array to match event.target
  let indexSquare = squares.findIndex(function(square) {
    return square === event.target;
  });
  board[indexSquare] = turn;
  turn = turn === "X" ? "O" : "X";
  //render that turn
  event.target.textContent = turn;
  win = getWinner();
  render();
}
document.querySelector("#board").addEventListener("click", handleTurn);

//use getWinner function to loop through winGame and check if player win on the board
function getWinner() {
  let winner = null;
  // loop through winGame, if 3 select match then win
  winGame.forEach(function(element, index) {
    //handle X or O match row or column or diagonal in any WinGame element then win the game
    if (
      board[element[0]] &&
      board[element[0]] === board[element[1]] &&
      board[element[0]] === board[element[2]]
    )
      winner = board[element[0]];
  });
  // includes() whether array includes a certain value among its entries,return true n false.
  if (winner) {
    return winner;
  }
  //add board.includes('') to return null, otherwise at the beginning it show no body win before we get someone win
  else if (board.includes("")) {
    return null;
  } else {
    return "noWinning";
  }
}

function render() {
  board.forEach(function(marks, index) {
    //set the text content of the square of the same position to the marks on the board.
    squares[index].textContent = marks;
  });
  // Conditional chains, like if,else if, else if, else
  messages.textContent =
    win === "noWinning"
      ? "No body win,please play again."
      : win
      ? `${win} wins the game!`
      : `It's ${turn}'s turn!`;
}
//init function to point each position in the JS array will correspond to a square on the HTML board
function init() {
  board = ["", "", "", "", "", "", "", "", ""];
  render();
}
init();

document.querySelector("#reset-button").addEventListener("click", init);
```
