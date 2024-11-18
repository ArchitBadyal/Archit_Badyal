<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Color Background</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Welcome to My Website</h1>
    <p>This website has a colored background.</p>
</body>
</html><!DOCTYPE html>
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
body {
  background-color: #3498db; /* Example: a shade of blue */
}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Color Background</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Welcome to My Website</h1>
    <p>This website has a colored background.</p>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Colorful Background</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, #ff9a9e, #fad0c4, #fad0c4, #fcb69f);
            background-size: 300% 300%;
            animation: gradient 10s ease infinite;
            color: white;
            font-family: Arial, sans-serif;
        }

        @keyframes gradient {
            0% {
                background-position: 0% 50%;
            }
            50% {
                background-position: 100% 50%;
            }
            100% {
                background-position: 0% 50%;
            }
        }

        h1 {
            font-size: 3rem;
        }
    </style>
</head>
<body>
    <h1>Welcome to My Colorful Website!</h1>
</body>
</html>
