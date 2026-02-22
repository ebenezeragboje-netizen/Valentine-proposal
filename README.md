<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Be My Valentine ❤️</title>
  <style>
    body {
      text-align: center;
      font-family: Arial, sans-serif;
      background: linear-gradient(to right, pink, red);
      color: white;
      height: 100vh;
      margin: 0;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }

    h1 {
      font-size: 2.5em;
      margin-bottom: 30px;
    }

    button {
      font-size: 20px;
      padding: 15px 30px;
      margin: 10px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    #yes {
      background-color: #00ff88;
      color: black;
      font-size: 22px;
    }

    #no {
      background-color: #ff4d4d;
      color: white;
    }
  </style>
</head>
<body>

  <h1>Will you be my Valentine? 💘</h1>

  <div>
    <button id="yes" onclick="yesClicked()">YES 💖</button>
    <button id="no" onclick="noClicked()">NO 💔</button>
  </div>

  <script>
    let yesSize = 22;
    let noSize = 20;

    function yesClicked() {
      document.body.innerHTML = `
        <h1>YAYYYY 🎉💖</h1>
        <h2>You just made me the happiest person 😍</h2>
        <h3>Happy Valentine’s Day 💐</h3>
      `;
    }

    function noClicked() {
      yesSize += 5;
      noSize -= 3;

      if (noSize < 8) noSize = 8;

      document.getElementById("yes").style.fontSize = yesSize + "px";
      document.getElementById("no").style.fontSize = noSize + "px";
    }
  </script>

</body>
</html>
