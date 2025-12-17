
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>John Doe | Portfolio</title>
    <style>
        /* Reset and Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: #333;
            background-color: #f9f9f9;
        }
        
        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background-color: #fff;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            font-size: 24px;
            font-weight: 700;
            color: #2c3e50;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            text-decoration: none;
            color: #2c3e50;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: #3498db;
        }
        
        /* Hero Section */
        .hero {
            padding: 150px 0 100px;
            text-align: center;
            background: linear-gradient(135deg, #3498db, #2c3e50);
            color: white;
        }
        
        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 20px;
            max-width: 700px;
            margin: 0 auto 30px;
        }
        
        .btn {
            display: inline-block;
            background: #fff;
            color: #3498db;
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
        }
        
        .btn:hover {
            background: #f1f1f1;
            transform: translateY(-3px);
        }
        
        /* About Section */
        .section {
            padding: 100px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .section-title h2 {
            font-size: 36px;
            color: #2c3e50;
            position: relative;
            display: inline-block;
            padding-bottom: 10px;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            width: 50%;
            height: 3px;
            background: #3498db;
            bottom: 0;
            left: 25%;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text h3 {
            font-size: 24px;
            margin-bottom: 20px;
            color: #2c3e50;
        }
        
        .about-image {
            flex: 1;
            text-align: center;
        }
        
        .profile-img {
            width: 300px;
            height: 300px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid #3498db;
        }
        
        /* Skills Section */
        .skills {
            background: #f1f1f1;
        }
        
        .skills-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
        }
        
        .skill {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            text-align: center;
            width: 200px;
            transition: transform 0.3s;
        }
        
        .skill:hover {
            transform: translateY(-10px);
        }
        
        .skill i {
            font-size: 40px;
            color: #3498db;
            margin-bottom: 15px;
        }
        
        /* Projects Section */
        .projects-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .project {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s;
        }
        
        .project:hover {
            transform: translateY(-10px);
        }
        
        .project-img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        
        .project-info {
            padding: 20px;
        }
        
        .project-info h3 {
            margin-bottom: 10px;
            color: #2c3e50;
        }
        
        /* Contact Section */
        .contact {
            background: #2c3e50;
            color: white;
        }
        
        .contact .section-title h2 {
            color: white;
        }
        
        .contact-form {
            max-width: 600px;
            margin: 0 auto;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-control {
            width: 100%;
            padding: 12px;
            border: none;
            border-radius: 5px;
            font-size: 16px;
        }
        
        textarea.form-control {
            height: 150px;
            resize: vertical;
        }
        
        .contact-btn {
            background: #3498db;
            color: white;
            border: none;
            cursor: pointer;
            transition: background 0.3s;
        }
        
        .contact-btn:hover {
            background: #2980b9;
        }
        
        /* Footer */
        footer {
            background: #1a252f;
            color: white;
            text-align: center;
            padding: 30px 0;
        }
        
        .social-links {
            margin-bottom: 20px;
        }
        
        .social-links a {
            color: white;
            font-size: 20px;
            margin: 0 10px;
            transition: color 0.3s;
        }
        
        .social-links a:hover {
            color: #3498db;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .about-content {
                flex-direction: column;
            }
            
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .hero p {
                font-size: 18px;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">Mahjabeen</div>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h1>Hi, I'm Mahjabeen</h1>
            <p>A passionate web developer creating beautiful and functional websites</p>
            <a href="#projects" class="btn">View My Work</a>
        </div>
    </section>

    <!-- About Section -->
    <section class="section" id="about">
        <div class="container">
            <div class="section-title">
                <h2>About Me</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>Hello! I'm Mahjabeen, a web designer.</h3>
                    <p>I have a passion for creating clean, beautiful, and user-friendly websites Design. I specialize in HTML and CSS.</p>
                    <p>When I'm not coding, you can find me exploring new technologies, reading tech blogs, or hiking in the mountains.</p>
                    <p>currently I'm student of intermediate and on the other hand im doing web development course in saylani it park</p>
                </div>
                <div class="about-image">
                    <img src="pm_1763646996057_cmp.jpg" alt="John Doe" class="profile-img">
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section class="section skills" id="skills">
        <div class="container">
            <div class="section-title">
                <h2>My Skills</h2>
            </div>
            <div class="skills-container">
                <div class="skill">
                    <i class="fab fa-html5"></i>
                    <h3>HTML5</h3>
                    <p>Semantic markup and accessibility</p>
                </div>
                <div class="skill">
                    <i class="fab fa-css3-alt"></i>
                    <h3>CSS3</h3>
                    <p>Responsive design and animations</p>
                </div>
                <div class="skill">
                    <i class="fab fa-js"></i>
                    <h3>Clean Code</h3>
                    <p>for beautiful web experiences</p>
                </div>
               
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section class="section" id="projects">
        <div class="container">
            <div class="section-title">
                <h2>My Projects</h2>
            </div>
            <div class="projects-container">
                <div class="project">
                    <video src="Parfumerie De Reve (1).mp4" alt="Project 1" controls class="project-img">
                    <div class="project-info">
                        <h3>E-commerce Website</h3>
                        <p>A fully responsive online store with shopping cart functionality.</p>
                    </div>
                </div>
                <div class="project">
                    <video src="Document (2).mp4" alt="Project 2" controls class="project-img">
                    <div class="project-info">
                        <h3>Flower bouquet website</h3>
                        <p>Design a bouquet off your choice</p>
                    </div>
                </div>
                
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="section contact" id="contact">
        <div class="section-title">
            <h2>Contact</h2>
        </div>
         <center><h3>Email me: awananna105@gmail.com</h3></center>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="#"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
            </div>
            <p>&copy; 2025 Mahjabeen. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
