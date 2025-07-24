<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Animated Portfolio</title>

    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">

    <style>
        /* General Body Styles */
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            background-color: #f8f8f8;
            color: #333;
            line-height: 1.6;
            scroll-behavior: smooth; /* Smooth scrolling for anchor links */
        }

        /* Container for content width */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header/Navigation Bar */
        .navbar {
            background-color: #fff;
            padding: 15px 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .navbar nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .navbar .logo {
            font-size: 1.8em;
            font-weight: 700;
            color: #007bff;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .navbar .logo:hover {
            color: #0056b3;
        }

        .navbar ul {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
        }

        .navbar ul li {
            margin-left: 30px;
        }

        .navbar ul li a {
            text-decoration: none;
            color: #555;
            font-weight: 600;
            font-size: 1.1em;
            position: relative;
            transition: color 0.3s ease;
        }

        .navbar ul li a:hover {
            color: #007bff;
        }

        .navbar ul li a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background-color: #007bff;
            left: 0;
            bottom: -5px;
            transition: width 0.3s ease;
        }

        .navbar ul li a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero-section {
            background: linear-gradient(135deg, #e0f2ff, #cceeff);
            min-height: 80vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 50px 20px;
            position: relative;
            overflow: hidden; /* Hide overflow for background animations */
        }

        /* Background animation for hero */
        .hero-section::before {
            content: '';
            position: absolute;
            top: -50px;
            left: -50px;
            width: 200px;
            height: 200px;
            background-color: rgba(0, 123, 255, 0.1);
            border-radius: 50%;
            animation: moveShape 10s infinite alternate ease-in-out;
            z-index: 0;
        }

        .hero-section::after {
            content: '';
            position: absolute;
            bottom: -50px;
            right: -50px;
            width: 150px;
            height: 150px;
            background-color: rgba(0, 123, 255, 0.08);
            border-radius: 50%;
            animation: moveShapeReverse 12s infinite alternate ease-in-out;
            z-index: 0;
        }

        @keyframes moveShape {
            0% { transform: translate(0, 0) scale(1); }
            50% { transform: translate(100px, 50px) scale(1.1); }
            100% { transform: translate(0, 0) scale(1); }
        }

        @keyframes moveShapeReverse {
            0% { transform: translate(0, 0) scale(1); }
            50% { transform: translate(-80px, -40px) scale(0.9); }
            100% { transform: translate(0, 0) scale(1); }
        }

        .hero-content {
            position: relative;
            z-index: 1; /* Ensure content is above background animations */
            max-width: 800px;
        }

        .hero-content h1 {
            font-size: 3.5em;
            margin-bottom: 15px;
            color: #007bff;
            font-weight: 700;
        }

        .hero-content .highlight {
            color: #28a745;
        }

        .hero-content .tagline {
            font-size: 1.5em;
            color: #666;
            margin-bottom: 30px;
        }

        .btn {
            display: inline-block;
            background-color: #007bff;
            color: #fff;
            padding: 12px 30px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            transition: background-color 0.3s ease, transform 0.3s ease;
        }

        .btn:hover {
            background-color: #0056b3;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        /* Section Styling */
        section {
            padding: 80px 0;
            border-bottom: 1px solid #eee;
        }

        section:last-of-type {
            border-bottom: none;
        }

        section h2 {
            font-size: 2.8em;
            text-align: center;
            margin-bottom: 60px;
            color: #007bff;
            position: relative;
            display: inline-block; /* For the underline effect */
            width: 100%; /* To center the inline-block */
        }

        section h2::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background-color: #28a745;
            margin: 15px auto 0;
            border-radius: 2px;
        }

        /* About Section */
        .about-section .container {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: center;
            gap: 40px;
            text-align: center;
        }

        .about-section .profile-image {
            flex: 1 1 300px;
            max-width: 300px;
            border-radius: 50%;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .about-section .profile-image:hover {
            transform: scale(1.03);
        }

        .about-section .profile-image img {
            width: 100%;
            height: auto;
            display: block;
        }

        .about-section .about-content {
            flex: 2 1 500px;
            max-width: 700px;
            text-align: left;
        }

        .about-section p {
            font-size: 1.1em;
            margin-bottom: 20px;
            color: #444;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 20px;
            margin-top: 40px;
        }

        .skill-item {
            background-color: #e9f5ff;
            border: 1px solid #cce9ff;
            padding: 15px;
            border-radius: 8px;
            text-align: center;
            font-weight: 600;
            color: #007bff;
            box-shadow: 0 4px 10px rgba(0, 123, 255, 0.08);
            transition: transform 0.3s ease, background-color 0.3s ease;
        }

        .skill-item:hover {
            transform: translateY(-5px) scale(1.02);
            background-color: #d8efff;
            box-shadow: 0 6px 15px rgba(0, 123, 255, 0.15);
        }

        /* Projects Section */
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            padding-top: 20px;
        }

        .project-card {
            background-color: #fff;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            text-align: center;
            padding-bottom: 20px;
        }

        .project-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 25px rgba(0, 0, 0, 0.15);
        }

        .project-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            display: block;
        }

        .project-card h3 {
            font-size: 1.8em;
            margin: 20px 0 10px;
            color: #007bff;
        }

        .project-card p {
            font-size: 1em;
            color: #555;
            padding: 0 20px 15px;
        }

        .project-card .btn {
            font-size: 0.9em;
            padding: 8px 20px;
        }

        /* Contact Section */
        .contact-section .container {
            text-align: center;
            max-width: 700px;
        }

        .contact-section p {
            font-size: 1.1em;
            margin-bottom: 40px;
            color: #444;
        }

        .contact-section form {
            display: flex;
            flex-direction: column;
            gap: 20px;
            background-color: #fff;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.08);
        }

        .contact-section input,
        .contact-section textarea {
            padding: 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1em;
            width: 100%;
            box-sizing: border-box; /* Include padding in width */
            transition: border-color 0.3s ease, box-shadow 0.3s ease;
        }

        .contact-section input:focus,
        .contact-section textarea:focus {
            border-color: #007bff;
            box-shadow: 0 0 0 3px rgba(0, 123, 255, 0.25);
            outline: none;
        }

        .contact-section textarea {
            resize: vertical; /* Allow vertical resizing */
            min-height: 120px;
        }

        .contact-section .btn {
            align-self: flex-end; /* Align button to the right */
            margin-top: 10px;
        }

        /* Footer */
        footer {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 30px 20px;
            font-size: 0.9em;
        }

        /* Responsive Adjustments */
        @media (max-width: 768px) {
            .navbar nav {
                flex-direction: column;
            }

            .navbar ul {
                margin-top: 15px;
                flex-wrap: wrap;
                justify-content: center;
            }

            .navbar ul li {
                margin: 0 15px 10px;
            }

            .hero-content h1 {
                font-size: 2.5em;
            }

            .hero-content .tagline {
                font-size: 1.2em;
            }

            section {
                padding: 60px 0;
            }

            section h2 {
                font-size: 2.2em;
            }

            .about-section .profile-image {
                margin-bottom: 30px;
            }

            .about-section .about-content {
                text-align: center;
            }
        }

        @media (max-width: 480px) {
            .hero-content h1 {
                font-size: 2em;
            }
            .hero-content .tagline {
                font-size: 1em;
            }
            section h2 {
                font-size: 1.8em;
            }
            .skill-item {
                font-size: 0.9em;
                padding: 10px;
            }
            .project-card h3 {
                font-size: 1.5em;
            }
            .contact-section input,
            .contact-section textarea,
            .contact-section .btn {
                font-size: 0.9em;
            }
        }

        /* Basic Fade-In on Load (for elements without specific AOS attributes) */
        @keyframes fadeInOnLoad {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .fade-in-on-load {
            animation: fadeInOnLoad 1s ease-out forwards;
        }
        .navbar, .hero-content h1, .hero-content .tagline, .hero-content .btn {
            /* These will get AOS animations, so skip the general fade-in */
        }
    </style>
</head>
<body>

    <header class="navbar fade-in-on-load">
        <nav>
            <a href="#home" class="logo">MyPortfolio</a>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="hero-section">
        <div class="hero-content">
            <h1 data-aos="fade-up" data-aos-duration="1000">Hi, I'm <span class="highlight">Your Name</span></h1>
            <p class="tagline" data-aos="fade-up" data-aos-delay="300" data-aos-duration="1000">A passionate Web Developer creating engaging digital experiences.</p>
            <a href="#projects" class="btn" data-aos="zoom-in" data-aos-delay="600" data-aos-duration="1000">View My Work</a>
        </div>
    </section>

    <section id="about" class="about-section">
        <div class="container">
            <h2 data-aos="fade-down">About Me</h2>
            <div class="profile-image" data-aos="fade-right" data-aos-duration="1000">
                <img src="https://via.placeholder.com/300x300?text=Your+Photo" alt="Your Photo">
            </div>
            <div class="about-content" data-aos="fade-left" data-aos-duration="1000" data-aos-delay="200">
                <p>
                    Hello! I'm a dedicated and enthusiastic web developer with a strong foundation in modern web technologies.
                    My journey in web development began with a fascination for how interactive and beautiful websites are built,
                    and it has since evolved into a passion for crafting efficient and user-friendly digital solutions.
                </p>
                <p>
                    I specialize in **front-end development**, bringing designs to life with clean, well-structured code. I'm
                    always eager to learn new technologies and improve my skills to deliver exceptional web experiences.
                </p>
                <h3>My Skills</h3>
                <div class="skills-grid">
                    <div class="skill-item" data-aos="zoom-in" data-aos-delay="300">HTML5</div>
                    <div class="skill-item" data-aos="zoom-in" data-aos-delay="400">CSS3</div>
                    <div class="skill-item" data-aos="zoom-in" data-aos-delay="500">JavaScript</div>
                    <div class="skill-item" data-aos="zoom-in" data-aos-delay="600">React</div>
                    <div class="skill-item" data-aos="zoom-in" data-aos-delay="700">Responsive Design</div>
                    <div class="skill-item" data-aos="zoom-in" data-aos-delay="800">Git & GitHub</div>
                </div>
            </div>
        </div>
    </section>

    <section id="projects" class="projects-section">
        <div class="container">
            <h2 data-aos="fade-down">My Projects</h2>
            <div class="project-grid">
                <div class="project-card" data-aos="fade-up" data-aos-duration="1000">
                    <img src="https://via.placeholder.com/400x200?text=Project+1" alt="Project 1">
                    <h3>E-commerce Store</h3>
                    <p>A fully responsive e-commerce platform with dynamic product listings and shopping cart functionality.</p>
                    <a href="#" class="btn" target="_blank">View Project</a>
                </div>
                <div class="project-card" data-aos="fade-up" data-aos-duration="1000" data-aos-delay="200">
                    <img src="https://via.placeholder.com/400x200?text=Project+2" alt="Project 2">
                    <h3>Task Management App</h3>
                    <p>A web application to help users organize tasks, set priorities, and track progress effectively.</p>
                    <a href="#" class="btn" target="_blank">View Project</a>
                </div>
                <div class="project-card" data-aos="fade-up" data-aos-duration="1000" data-aos-delay="400">
                    <img src="https://via.placeholder.com/400x200?text=Project+3" alt="Project 3">
                    <h3>Personal Blog</h3>
                    <p>A clean and modern blog platform built for sharing articles and insights on various tech topics.</p>
                    <a href="#" class="btn" target="_blank">View Project</a>
                </div>
                </div>
        </div>
    </section>

    <section id="contact" class="contact-section">
        <div class="container">
            <h2 data-aos="fade-down">Get In Touch</h2>
            <p data-aos="fade-up" data-aos-delay="200">
                Have a project in mind or just want to say hello? Feel free to reach out!
                I'm always open to new opportunities and collaborations.
            </p>
            <form data-aos="fade-up" data-aos-delay="400">
                <input type="text" placeholder="Your Name" required>
                <input type="email" placeholder="Your Email" required>
                <textarea placeholder="Your Message" rows="6"></textarea>
                <button type="submit" class="btn">Send Message</button>
            </form>
        </div>
    </section>

    <footer>
        <p>&copy; 2025 Your Name. All rights reserved.</p>
    </footer>

    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
        // Initialize AOS
        AOS.init({
            duration: 1200, // values from 0 to 3000, with step 50ms
            once: true,    // whether animation should happen only once - while scrolling down
            mirror: false, // whether elements should animate out while scrolling past them
        });

        // Smooth scrolling for navigation links
        document.querySelectorAll('.navbar a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
