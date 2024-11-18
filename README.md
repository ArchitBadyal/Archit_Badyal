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
