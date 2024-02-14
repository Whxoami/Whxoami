<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Be My Valentine</title>
<style>
  body {
    font-family: Arial, sans-serif;
    text-align: center;
    margin: 50px;
  }
  h1 {
    color: #e60000;
  }
  button {
    background-color: #e70000;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    margin: 10px;
  }
  button:hover {
    background-color: #cc0000;
  }
  #cat-gif {
    max-width: 300px;
    display: none;
  }
</style>
</head>
<body>
<h1>Be My Valentine?</h1>
<button onclick="sayYes()">Yes</button>
<button onclick="sayNo()">No</button>
<p id="message"></p>
<div id="cat-gif">
  <img src="https://media.giphy.com/media/vFKqnCdLPNOKc/giphy.gif" alt="Cute cat begging">
</div>
<script>
  var options = [
    "Will you be my valentine?",
    "Can we spend the day eating chocolate?",
    "How about a romantic dinner?",
    "Shall we watch a cheesy romantic movie?",
    "Wanna dance like nobody's watching?",
    "Would you accept this virtual bouquet of flowers?",
    "How about we play some love songs and serenade each other?",
    "Shall we exchange cheesy Valentine's Day cards?"
  ];

  var message = document.getElementById("message");
  var catGif = document.getElementById("cat-gif");

  function presentOption() {
    var index = Math.floor(Math.random() * options.length);
    message.innerHTML = options[index];
  }

  function sayYes() {
    message.innerHTML = "ingel chi mnihshude kk";
    var optionsHtml = `
      <button onclick="playChess()">Can we play chess together sitting in front of each other <3</button>
      <button onclick="hugUntilSleep()">Let me hug you until we'll fall asleep</button>
      <button onclick="singASong()">Hoyulangn songchoy kkk</button>
    `;
    message.insertAdjacentHTML('beforeend', optionsHtml);
  }

  function sayNo() {
    catGif.style.display = "block";
    message.innerHTML = "mayglad bailgu tiim geech";
    setTimeout(presentOption, 3000); // Change option after 5 seconds
  }

  function playChess() {
    message.innerHTML = "Great choice! Let's play chess and have a romantic time together.";
  }

  function hugUntilSleep() {
    message.innerHTML = "no prob bae";
  }

  function singASong() {
    message.innerHTML = "okeelov uu byee";
  }
</script>
</body>
</html>
