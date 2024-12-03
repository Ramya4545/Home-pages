<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Navigation Menu</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header class="navbar">
        <nav>
            <ul class="menu">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>
    <section id="home">
        <h1>Welcome to the Home Page</h1>
        <p>Scroll down to see the interactive navigation bar in action.</p>
    </section>
    <section id="about">
        <h1>About Us</h1>
        <p>Learn more about our story and mission.</p>
    </section>
    <section id="services">
        <h1>Our Services</h1>
        <p>Explore what we offer to our customers.</p>
    </section>
    <section id="contact">
        <h1>Contact Us</h1>
        <p>Reach out to us with your inquiries.</p>
    </section>
    <script src="script.js"></script>
</body>
</html>

body {
    margin: 0;
    font-family: Arial, sans-serif;
    line-height: 1.6;
}

section {
    height: 100vh;
    padding: 20px;
    text-align: center;
}

/* Navigation Bar */
.navbar {
    position: fixed;
    top: 0;
    width: 100%;
    background-color: rgba(255, 255, 255, 0.8);
    transition: background-color 0.3s ease;
    z-index: 1000;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.menu {
    list-style: none;
    display: flex;
    justify-content: center;
    margin: 0;
    padding: 10px 0;
}

.menu li {
    margin: 0 20px;
}

.menu a {
    text-decoration: none;
    color: #333;
    font-weight: bold;
    transition: color 0.3s ease, transform 0.3s ease;
}

.menu a:hover {
    color: #007bff;
    transform: scale(1.1);
}

/* Active on Scroll */
.navbar.scrolled {
    background-color: rgba(0, 123, 255, 0.9);
}

.navbar.scrolled .menu a {
    color: #fff;
}



const navbar = document.querySelector('.navbar');

// Add an event listener for scroll events
window.addEventListener('scroll', () => {
    if (window.scrollY > 50) {
        navbar.classList.add('scrolled');
    } else {
        navbar.classList.remove('scrolled');
    }
});

