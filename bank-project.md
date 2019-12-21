```
//html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>NAB ONLINEBANK</title>
    <link rel="stylesheet" href="style1.css" />
  </head>
  <body>
    <header className="App-header">
      <a href="https://www.nab.com.au" target="_blank">
        <img
          src="data:image/png;base64,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"
          alt="logo"
        />
      </a>
    </header>
    <h1>ONLINE BANK</h1>
    <div class="container">
      <section class="saving">
        <h3>SAVING</h3>
        <h4>YOUR BALANCE IS ...</h4>
        <div class="savingTotal">
          Total: <span class="savingBalance">0</span>
        </div>
        $<input
          style="background-color: aqua"
          id="savingDeposit"
          type="number"
          value="number"
        />
        <button class="savingDeposit-btn">DEPOSIT</button>
        <button class="savingWithdraw-btn">WITHDRAW</button>
      </section>
      <section class="check">
        <h3>CHECKING</h3>
        <h4>YOUR BALANCE IS ...</h4>
        <div class="checkTotal">Total: <span class="checkBalance">0</span></div>
        $<input
          style="background-color: aqua "
          id="checkDeposit"
          type="number"
          value="number"
        />
        <button class="checkDeposit-btn">DEPOSIT</button>
        <button class="checkWithdraw-btn">WITHDRAW</button>
      </section>

      <script src="bank.js"></script>
    </div>
  </body>
</html>
```
//css
```
h1 {
  text-align: center;
}
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
}
div {
  font-size: 15px;
}
.saving {
  background-color: orange;
  width: 400px;
  height: 300px;
  justify-content: center;
  font-size: 20px;
  border: 2px solid black;
}
.check {
  background-color: yellow;
  width: 400px;
  height: 300px;
  justify-content: center;
  font-size: 20px;
  border: 2px solid black;
}
h3 {
  text-align: center;
}
p {
  font-size: 15px;
}
.savingDeposit-btn {
  background-color: rgb(187, 173, 173);
}
.savingWithdraw-btn {
  background-color: rgb(187, 173, 173);
}
.checkDeposit-btn {
  background-color: rgb(187, 173, 173);
}
.checkWithdraw-btn {
  background-color: rgb(187, 173, 173);
}

```
//bank.js
```
var savingTotalBalance = 0;
var savingDeposit = 0;
var savingWithdraw = 0;
var savingDepositBtn = document.querySelector(".savingDeposit-btn");
var savingWithdrawBtn = document.querySelector(".savingWithdraw");
var savingBalanceElement = document.querySelector(".savingBalance");
var savingWithdrawElement = document.querySelector(".savingBalance");

var handleSaving = function() {
  savingDeposit = Number(document.querySelector("#savingDeposit").value);
  var savingCurrentBalance = Number(savingBalanceElement.textContent);
  var newSavingBalance = savingDeposit + savingCurrentBalance;
  savingBalanceElement.textContent = newSavingBalance;
};
var handleSavingWithdraw = function() {
  savingDeposit = Number(document.querySelector("#savingDeposit").value);
  var savingCurrentBalance = Number(savingBalanceElement.textContent);
  var newSavingBalance = savingDeposit + savingCurrentBalance;
  savingBalanceElement.textContent = newSavingBalance;
  savingWithdraw = Number(document.querySelector("#savingWithdraw").value);
  var newWithdrawBalance = newSavingBalance - savingWithdraw;
  savingBalanceElement.textContent = newWithdrawBalance;
};
savingDepositBtn.addEventListener("click", handleSaving);
// savingWithdrawBtn.addEventListener("click", handleSavingWithdraw);

var checkTotalBalance = 0;
var checkDeposit = 0;
var checkWithdraw = 0;
var checkDepositBtn = document.querySelector(".checkDeposit-btn");
// var checkWithdrawBtn = document.querySelector(".checkWithdraw");
var checkBalanceElement = document.querySelector(".checkBalance");
// var checkWithdrawElement = document.querySelector(".checkBalance");

var handleCheck = function() {
  checkDeposit = Number(document.querySelector("#checkDeposit").value);
  var checkCurrentBalance = Number(checkBalanceElement.textContent);
  var newcheckBalance = checkDeposit + checkCurrentBalance;
  checkBalanceElement.textContent = newcheckBalance;
};
checkDepositBtn.addEventListener("click", handleCheck);
```
