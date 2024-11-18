<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Personal Website</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Welcome to My Website</h1>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home">
        <h2>Hello, I'm Archit</h2>
        <p>Welcome to my personal space on the internet. I love coding, detective novels, and exploring new ideas.</p>
    </section>

    <section id="about">
        <h2>About Me</h2>
        <p>I am an introvert who enjoys reading and spending time on interesting projects. Currently exploring web development!</p>
    </section>

    <section id="projects">
        <h2>My Projects</h2>
        <ul>
            <li>Project 1: <a href="#">GitHub Repo</a></li>
            <li>Project 2: <a href="#">GitHub Repo</a></li>
        </ul>
    </section>

    <section id="contact">
        <h2>Contact Me</h2>
        <form>
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
            <textarea placeholder="Your Message" required></textarea>
            <button type="submit">Send</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2024 Archit. All rights reserved.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Archit's Portfolio</title>
    <link rel="stylesheet" href="styles.css">
    <link rel="icon" href="images/favicon.png">
</head>
<body>

    <!-- Navigation Bar -->
    <header>
        <nav>
            <h1>Archit</h1>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <h2>Welcome to My Personal Website</h2>
        <p>I’m Archit, a passionate coder and avid reader.</p>
        <a href="#projects" class="btn">Explore My Work</a>
    </section>

    <!-- About Section -->
    <section id="about">
        <h2>About Me</h2>
        <p>I am an introvert who enjoys reading detective novels and diving deep into web development. I love solving problems and creating elegant solutions.</p>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <h2>Projects</h2>
        <div class="project-grid">
            <div class="project">
                <img src="images/project1.jpg" alt="Project 1">
                <h3>Project 1</h3>
                <p>A cool project I worked on.</p>
            </div>
            <div class="project">
                <img src="images/project2.jpg" alt="Project 2">
                <h3>Project 2</h3>
                <p>Another amazing project.</p>
            </div>
            <div class="project">
                <img src="images/project3.jpg" alt="Project 3">
                <h3>Project 3</h3>
                <p>My latest creation.</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2>Contact Me</h2>
        <form>
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
            <textarea placeholder="Your Message" required></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2024 Archit. All rights reserved.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Snake Game</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background-color: #111;
      font-family: Arial, sans-serif;
    }
    .game-container {
      position: relative;
      width: 400px;
      height: 400px;
      background-color: #222;
      border: 2px solid #888;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
    }
    .snake {
      width: 20px;
      height: 20px;
      background-color: #4caf50;
      position: absolute;
    }
    .food {
      width: 20px;
      height: 20px;
      background-color: #f44336;
      position: absolute;
    }
  </style>
</head>
<body>
  <div class="game-container">
    <div class="score">Score: 0</div>
    <div class="food"></div>
  </div>

  <script>
    const gameContainer = document.querySelector('.game-container');
    const foodElement = document.querySelector('.food');
    const scoreElement = document.querySelector('.score');

    const gridSize = 20;
    const gameSize = 400;

    let snake = [{ x: 60, y: 60 }];
    let food = { x: 0, y: 0 };
    let direction = { x: gridSize, y: 0 };
    let score = 0;

    function getRandomPosition() {
      return Math.floor(Math.random() * (gameSize / gridSize)) * gridSize;
    }

    function placeFood() {
      food.x = getRandomPosition();
      food.y = getRandomPosition();
      foodElement.style.left = `${food.x}px`;
      foodElement.style.top = `${food.y}px`;
    }

    function drawSnake() {
      gameContainer.querySelectorAll('.snake').forEach(el => el.remove());

      snake.forEach(segment => {
        const snakeElement = document.createElement('div');
        snakeElement.classList.add('snake');
        snakeElement.style.left = `${segment.x}px`;
        snakeElement.style.top = `${segment.y}px`;
        gameContainer.appendChild(snakeElement);
      });
    }

    function moveSnake() {
      const head = { x: snake[0].x + direction.x, y: snake[0].y + direction.y };

      // Check collision with walls or itself
      if (
        head.x < 0 || head.x >= gameSize || head.y < 0 || head.y >= gameSize ||
        snake.some(segment => segment.x === head.x && segment.y === head.y)
      ) {
        alert('Game Over! Final Score: ' + score);
        location.reload();
        return;
      }

      snake.unshift(head);

      // Check if snake eats the food
      if (head.x === food.x && head.y === food.y) {
        score++;
        scoreElement.textContent = `Score: ${score}`;
        placeFood();
      } else {
        snake.pop();
      }

      drawSnake();
    }

    function changeDirection(e) {
      switch (e.key) {
        case 'ArrowUp':
          if (direction.y === 0) direction = { x: 0, y: -gridSize };
          break;
        case 'ArrowDown':
          if (direction.y === 0) direction = { x: 0, y: gridSize };
          break;
        case 'ArrowLeft':
          if (direction.x === 0) direction = { x: -gridSize, y: 0 };
          break;
        case 'ArrowRight':
          if (direction.x === 0) direction = { x: gridSize, y: 0 };
          break;
      }
    }

    document.addEventListener('keydown', changeDirection);

    function gameLoop() {
      moveSnake();
      setTimeout(gameLoop, 200);
    }

    placeFood();
    gameLoop();
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mini Car Game</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background-color: #111;
      font-family: Arial, sans-serif;
    }
    .game-container {
      position: relative;
      width: 400px;
      height: 600px;
      background-color: #333;
      overflow: hidden;
      border: 2px solid #888;
    }
    .road {
      position: absolute;
      top: 0;
      left: 50%;
      width: 200px;
      height: 100%;
      background-color: #555;
      transform: translateX(-50%);
    }
    .lane {
      position: absolute;
      width: 5px;
      height: 30px;
      background-color: #fff;
      top: 0;
      left: 50%;
      transform: translateX(-50%);
      animation: laneMove 1s linear infinite;
    }
    @keyframes laneMove {
      0% {
        top: -30px;
      }
      100% {
        top: 600px;
      }
    }
    .car {
      position: absolute;
      bottom: 20px;
      left: 170px;
      width: 50px;
      height: 80px;
      background-color: #f44336;
      border-radius: 5px;
    }
    .obstacle {
      position: absolute;
      width: 50px;
      height: 80px;
      background-color: #000;
      border-radius: 5px;
      animation: obstacleMove 2s linear infinite;
    }
    @keyframes obstacleMove {
      0% {
        top: -80px;
      }
      100% {
        top: 600px;
      }
    }
    .score {
      position: absolute;
      top: 10px;
      left: 10px;
      color: #fff;
      font-size: 18px;
    }
  </style>
</head>
<body>
  <div class="game-container">
    <div class="road"></div>
    <div class="score">Score: 0</div>
    <div class="car"></div>
  </div>

  <script>
    const gameContainer = document.querySelector('.game-container');
    const car = document.querySelector('.car');
    const scoreElement = document.querySelector('.score');
    const gameWidth = 400;
    const carWidth = 50;
    const carStep = 30;
    let score = 0;
    let gameOver = false;

    function getRandomPosition() {
      return Math.floor(Math.random() * (gameWidth / carWidth)) * carWidth;
    }

    function createObstacle() {
      const obstacle = document.createElement('div');
      obstacle.classList.add('obstacle');
      obstacle.style.left = `${getRandomPosition()}px`;
      gameContainer.appendChild(obstacle);
      return obstacle;
    }

    function moveObstacle(obstacle) {
      const move = setInterval(() => {
        const obstacleTop = obstacle.offsetTop;
        const carLeft = car.offsetLeft;
        const carBottom = car.offsetTop + car.offsetHeight;
        const obstacleLeft = obstacle.offsetLeft;
        const obstacleBottom = obstacleTop + obstacle.offsetHeight;

        if (obstacleTop > 600) {
          clearInterval(move);
          obstacle.remove();
          score++;
          scoreElement.textContent = `Score: ${score}`;
        }

        if (
          obstacleTop > carBottom - 80 &&
          obstacleTop < carBottom &&
          obstacleLeft === carLeft
        ) {
          alert(`Game Over! Final Score: ${score}`);
          location.reload();
        }
        obstacle.style.top = `${obstacleTop + 10}px`;
      }, 50);
    }

    function moveCar(e) {
      if (e.key === 'ArrowLeft') {
        car.style.left = `${Math.max(car.offsetLeft - carStep, 0)}px`;
      } else if (e.key === 'ArrowRight') {
        car.style.left = `${Math.min(
          car.offsetLeft + carStep,
          gameWidth - carWidth
        )}px`;
      }
    }

    function createLanes() {
      for (let i = 0; i < 20; i++) {
        const lane = document.createElement('div');
        lane.classList.add('lane');
        lane.style.top = `${i * 30}px`;
        document.querySelector('.road').appendChild(lane);
      }
    }

    document.addEventListener('keydown', moveCar);

    createLanes();

    setInterval(() => {
      const obstacle = createObstacle();
      moveObstacle(obstacle);
    }, 3000);
  </script>
</body>
</html>
