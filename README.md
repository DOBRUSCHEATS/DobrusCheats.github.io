<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>You got scamed</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background-color: black;
      color: #00ff00;
      font-family: monospace;
      font-size: 24px;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      text-align: center;
      flex-direction: column;
    }

    .ip {
      margin-top: 20px;
      color: red;
      font-size: 20px;
    }
  </style>
</head>
<body>
  <div>
    <p>you got scamed<br>and your ip is mine now</p>
    <div class="ip" id="ip"></div>
  </div>

  <script>
    function getRandomIP() {
      return Array(4).fill(0).map(() => Math.floor(Math.random() * 256)).join('.');
    }

    document.getElementById('ip').textContent = 'IP: ' + getRandomIP();
  </script>
</body>
</html>
