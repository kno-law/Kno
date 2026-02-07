# Kno
Practice for the future 
<!DOCTYPE html>
<html>
<head>
  <title>Tambola Game</title>
  <style>
    body { font-family: Arial; text-align: center; background: #f4f4f4; }
    button { padding: 10px 20px; font-size: 18px; margin: 10px; }
    .number { font-size: 40px; color: green; margin: 20px; }
    .called { max-width: 300px; margin: auto; }
    span { padding: 5px; display: inline-block; }
  </style>
</head>
<body>

<h1>🎉 Tambola Game 🎉</h1>

<button onclick="callNumber()">Call Number</button>

<div class="number" id="current">--</div>

<h3>Called Numbers</h3>
<div class="called" id="calledNumbers"></div>

<script>
let numbers = [];
for (let i = 1; i <= 90; i++) numbers.push(i);

function callNumber() {
  if (numbers.length === 0) {
    alert("All numbers called!");
    return;
  }
  let index = Math.floor(Math.random() * numbers.length);
  let num = numbers.splice(index, 1)[0];
  document.getElementById("current").innerText = num;
  document.getElementById("calledNumbers").innerHTML += "<span>" + num + "</span>";
}
</script>

</body>
</html>
