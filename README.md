<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Colorful Background</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: Arial, sans-serif;
      background: linear-gradient(45deg, #ff7eb3, #ff758f, #ffa454, #ffff54, #54ff7e, #54ffff, #547eff, #7e54ff, #ff54ff);
      background-size: 400% 400%;
      animation: gradientAnimation 10s ease infinite;
    }

    @keyframes gradientAnimation {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    h1 {
      color: white;
      text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
    }
  </style>
</head>
<body>
  <h1>Colorful Background</h1>
</body>
</html>