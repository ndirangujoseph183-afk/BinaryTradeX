let balance = 1000;

document.getElementById("balance").innerText = "$" + balance;

function trade(direction) {
    let result = document.getElementById("result");

    // random market movement (demo logic)
    let outcome = Math.random() < 0.5 ? "UP" : "DOWN";

    if (direction === outcome) {
        balance += 50; // win
        result.innerHTML = "✅ You WON! Market was " + outcome;
        result.style.color = "green";
    } else {
        balance -= 50; // lose
        result.innerHTML = "❌ You LOST! Market was " + outcome;
        result.style.color = "red";
    }

    document.getElementById("balance").innerText = "$" + balance;
}<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>NovaTrade</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <div class="navbar">
    <h2>NovaTrade</h2>
    <button onclick="login()">Login</button>
  </div>

  <div class="container">
    <h1>Welcome to NovaTrade Platform</h1>
    <p>Simple trading dashboard UI (demo version)</p>

    <div class="card">
      <h3>Account Balance</h3>
      <p id="balance">$1,000</p>
    </div>

    <div class="card">
      <h3>Quick Trade</h3>
      <button onclick="trade('UP')">UP</button>
      <button onclick="trade('DOWN')">DOWN</button>
    </div>

    <p id="result"></p>
  </div>

  <script src="script.js"></script>
</body>
</html># BinaryTradeX
Its a trading platform i want to create a link for
