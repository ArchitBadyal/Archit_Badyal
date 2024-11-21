<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dangerous Skull Logo</title>
  <style>
    body {
      margin: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: black;
      color: white;
      font-family: 'Arial', sans-serif;
    }

    .skull-logo {
      position: relative;
      width: 200px;
      height: 250px;
      background: radial-gradient(circle at top, #222, #000);
      border-radius: 50%;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
      box-shadow: 0 0 20px rgba(255, 0, 0, 0.8);
    }

    /* Eyes */
    .eye {
      position: absolute;
      top: 30%;
      width: 40px;
      height: 40px;
      background: red;
      border-radius: 50%;
      box-shadow: inset 0 0 10px black;
    }

    .eye.left {
      left: 30%;
    }

    .eye.right {
      right: 30%;
    }

    /* Nose */
    .nose {
      position: absolute;
      top: 50%;
      width: 20px;
      height: 30px;
      background: red;
      clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
    }

    /* Teeth */
    .teeth {
      position: absolute;
      bottom: 10%;
      display: flex;
      gap: 5px;
    }

    .tooth {
      width: 20px;
      height: 30px;
      background: red;
      clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
    }

    /* AB Text */
    .skull-logo span {
      position: absolute;
      bottom: 35%;
      color: white;
      font-size: 40px;
      font-weight: bold;
      text-shadow: 0 0 10px rgba(255, 255, 255, 0.8);
    }
  </style>
</head>
<body>
  <div class="skull-logo">
    <div class="eye left"></div>
    <div class="eye right"></div>
    <div class="nose"></div>
    <div class="teeth">
      <div class="tooth"></div>
      <div class="tooth"></div>
      <div class="tooth"></div>
      <div class="tooth"></div>
    </div>
    <span>AB</span>
  </div>
</body>
</html>
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
      color: black;
      text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
    }
  </style>
</head>
<body>
  <h1>Welcome Friends</h1>
</body>
</html>

<p>This website provide you Bca modal paper or previous paper for study Well. </p>


<h1>BCA 1st Semester</h1>
