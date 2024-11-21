<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Open Book Logo</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background-color: #f3f4f6;
      font-family: Arial, sans-serif;
    }

    .book-container {
      position: relative;
      width: 300px;
      height: 200px;
      perspective: 800px;
    }

    .book {
      position: absolute;
      width: 100%;
      height: 100%;
      transform-style: preserve-3d;
      display: flex;
    }

    /* Left Page */
    .left-page {
      position: absolute;
      width: 50%;
      height: 100%;
      background: linear-gradient(to right, #fff 80%, #e0e0e0);
      transform-origin: right;
      box-shadow: -3px 0px 5px rgba(0, 0, 0, 0.1);
    }

    /* Right Page */
    .right-page {
      position: absolute;
      right: 0;
      width: 50%;
      height: 100%;
      background: linear-gradient(to left, #fff 80%, #e0e0e0);
      transform-origin: left;
      box-shadow: 3px 0px 5px rgba(0, 0, 0, 0.1);
    }

    /* Center Fold */
    .center-fold {
      position: absolute;
      top: 0;
      left: 50%;
      width: 2px;
      height: 100%;
      background: #ccc;
      box-shadow: 0 0 3px rgba(0, 0, 0, 0.3);
      transform: translateX(-50%);
    }

    /* Book Content */
    .page-content {
      position: absolute;
      top: 10%;
      left: 5%;
      right: 5%;
      bottom: 10%;
      font-size: 14px;
      color: #333;
      line-height: 1.5;
      overflow: hidden;
    }

    .left-page .page-content {
      text-align: right;
    }

    .right-page .page-content {
      text-align: left;
    }
  </style>
</head>
<body>
  <div class="book-container">
    <div class="book">
      <div class="left-page">
        <div class="page-content">
          <p>Chapter 1</p>
          <p>Once upon a time in a land far away...</p>
        </div>
      </div>
      <div class="right-page">
        <div class="page-content">
          <p>Introduction</p>
          <p>...there lived a storyteller with magical tales.</p>
        </div>
      </div>
      <div class="center-fold"></div>
    </div>
  </div>
</body>
</html>
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
      border-r
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
