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
      position: relative;
    }

    .ip {
      margin-top: 20px;
      color: red;
      font-size: 20px;
    }

    .moving-text {
      position: absolute;
      top: 0;
      left: 100%;
      font-size: 36px;
      color: #ff0000;
      font-family: monospace;
      animation: moveText 5s linear infinite;
    }

    @keyframes moveText {
      0% {
        left: 100%;
      }
      100% {
        left: -100%;
      }
    }
  </style>
</head>
<body>
  <div class="moving-text">
    pay 10 bitcoins or get bombed
  </div>
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
