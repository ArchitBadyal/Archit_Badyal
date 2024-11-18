Archit Badyal
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Green Background</title>
    <style>
        body {
            background-color: orange;
            color: black; /* Optional: Text color for better contrast */
        }
    </style>
</head>
<body>
    <h1>Welcome to my Website Friends </h1>
    <p>This page provide you old question paper solved.</p>
</body>
</html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Computer fundamental 1</title>
</head>
<body>
    <h1>Computer Fundamental 1</h1></h1>
    <iframe src="https://coffee-shina-74.tiiny.site" width="30%" height="100px"></iframe>
</body>
</html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Computer fundamental 2</title>
</head>
<body>
    <h1>Computer fundamental 2</h1>
    <iframe src="https://drive.google.com/file/d/12E0wN6fsWQ8zFg9P4vN2JSQrK977qi0E/view?usp=drivesdk" width="100%" height="600px"></iframe>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tic Tac Toe - Player vs Robot</title>
    <style>
        * {
            box-sizing: border-box;
        }
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
        }
        .container {
            display: grid;
            grid-template-columns: repeat(3, 100px);
            grid-gap: 5px;
        }
        .cell {
            width: 100px;
            height: 100px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 2em;
            background-color: #fff;
            border: 2px solid #ddd;
            cursor: pointer;
            user-select: none;
        }
        .cell:hover {
            background-color: #f9f9f9;
        }
        .message {
            margin-top: 20px;
            font-size: 1.2em;
            text-align: center;
        }
        .reset {
            display: block;
            margin: 20px auto;
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            border: none;
            cursor: pointer;
        }
        .reset:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div>
        <div class="container" id="board">
            <div class="cell" data-index="0"></div>
            <div class="cell" data-index="1"></div>
            <div class="cell" data-index="2"></div>
            <div class="cell" data-index="3"></div>
            <div class="cell" data-index="4"></div>
            <div class="cell" data-index="5"></div>
            <div class="cell" data-index="6"></div>
            <div class="cell" data-index="7"></div>
            <div class="cell" data-index="8"></div>
        </div>
        <div class="message" id="message"></div>
        <button class="reset" onclick="resetGame()">Restart Game</button>
    </div>

    <script>
        const board = document.getElementById('board');
        const cells = document.querySelectorAll('.cell');
        const message = document.getElementById('message');
        let currentPlayer = 'X';
        let gameActive = true;
        let gameBoard = ['', '', '', '', '', '', '', '', ''];

        const winningCombinations = [
            [0, 1, 2],
            [3, 4, 5],
            [6, 7, 8],
            [0, 3, 6],
            [1, 4, 7],
            [2, 5, 8],
            [0, 4, 8],
            [2, 4, 6]
        ];

        // Check for winner or draw
        function checkWinner() {
            for (let combination of winningCombinations) {
                const [a, b, c] = combination;
                if (gameBoard[a] && gameBoard[a] === gameBoard[b] && gameBoard[a] === gameBoard[c]) {
                    gameActive = false;
                    message.textContent = `${gameBoard[a]} wins!`;
                    return true;
                }
            }
            if (!gameBoard.includes('')) {
                gameActive = false;
                message.textContent = "It's a draw!";
                return true;
            }
            return false;
        }

        // Robot (AI) makes a move
        function robotMove() {
            let emptyCells = [];
            gameBoard.forEach((cell, index) => {
                if (cell === '') emptyCells.push(index);
            });

            if (emptyCells.length > 0) {
                const randomIndex = emptyCells[Math.floor(Math.random() * emptyCells.length)];
                gameBoard[randomIndex] = 'O';
                cells[randomIndex].textContent = 'O';
                cells[randomIndex].style.pointerEvents = 'none';
                checkWinner();
                currentPlayer = 'X';
            }
        }

        // Handle cell click
        function handleCellClick(event) {
            const index = event.target.dataset.index;
            if (gameBoard[index] === '' && gameActive) {
                gameBoard[index] = currentPlayer;
                event.target.textContent = currentPlayer;
                event.target.style.pointerEvents = 'none';

                if (checkWinner()) return;

                currentPlayer = 'O';
                setTimeout(robotMove, 500);
            }
        }

        // Attach event listeners to cells
        cells.forEach(cell => {
            cell.addEventListener('click', handleCellClick);
        });

        // Reset the game
        function resetGame() {
            gameBoard = ['', '', '', '', '', '', '', '', ''];
            cells.forEach(cell => {
                cell.textContent = '';
                cell.style.pointerEvents = 'auto';
            });
            currentPlayer = 'X';
            gameActive = true;
            message.textContent = '';
        }
    </script>
</body>
</html>
