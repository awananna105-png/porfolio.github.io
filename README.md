
          <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mahjabeen - Web Designer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f8f9fa;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Header Section */
        header {
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            color: white;
            padding: 30px 0;
            text-align: center;
        }
        
        .header-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 80vh;
        }
        
        h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            letter-spacing: 2px;
        }
        
        .tagline {
            font-size: 1.8rem;
            margin-bottom: 30px;
            font-weight: 300;
        }
        
        .btn {
            display: inline-block;
            background-color: #ff6b6b;
            color: white;
            padding: 15px 35px;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1.2rem;
            margin-top: 20px;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .btn:hover {
            background-color: #ff5252;
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
        }
        
        /* About Section */
        .section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 50px;
            color: #2575fc;
            position: relative;
        }
        
        .section-title:after {
            content: '';
            position: absolute;
            width: 80px;
            height: 4px;
            background-color: #ff6b6b;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 2px;
        }
        
        .about-content {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 40px;
        }
        
        .about-text {
            flex: 1;
            min-width: 300px;
            font-size: 1.1rem;
        }
        
        .about-text p {
            margin-bottom: 20px;
            font-size: 1.1rem;
            line-height: 1.8;
        }
        
        /* Skills Section */
        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            justify-content: center;
        }
        
        .skill-card {
            background-color: white;
            border-radius: 15px;
            padding: 30px;
            width: 300px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            text-align: center;
            transition: transform 0.3s ease;
        }
        
        .skill-card:hover {
            transform: translateY(-10px);
        }
        
        .skill-icon {
            font-size: 3rem;
            margin-bottom: 20px;
            color: #2575fc;
        }
        
        .skill-title {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: #333;
        }
        
        .skill-desc {
            color: #666;
            font-size: 1rem;
        }
        
        /* Projects Section */
        .projects-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .project-card {
            background-color: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-10px);
        }
        
        .project-placeholder {
            height: 200px;
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            font-weight: 600;
        }
        
        .project-info {
            padding: 25px;
        }
        
        .project-title {
            font-size: 1.4rem;
            margin-bottom: 10px;
            color: #333;
        }
        
        .project-desc {
            color: #666;
            font-size: 1rem;
        }
        
        /* Footer */
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 40px 0;
            margin-top: 60px;
        }
        
        .footer-text {
            font-size: 1.1rem;
            margin-bottom: 20px;
        }
        
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        
        .social-icons a {
            color: white;
            font-size: 1.5rem;
            transition: color 0.3s ease;
        }
        
        .social-icons a:hover {
            color: #ff6b6b;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }
            
            .tagline {
                font-size: 1.4rem;
            }
            
            .header-content {
                min-height: 60vh;
            }
            
            .section {
                padding: 50px 0;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .skill-card {
                width: 100%;
                max-width: 400px;
            }
            
            .projects-container {
                grid-template-columns: 1fr;
            }
            
            .about-text {
                min-width: 100%;
            }
        }
        
        @media (max-width: 480px) {
            h1 {
                font-size: 2rem;
            }
            
            .tagline {
                font-size: 1.2rem;
            }
            
            .btn {
                padding: 12px 25px;
                font-size: 1rem;
            }
            
            .section-title {
                font-size: 1.8rem;
            }
            
            .about-text p {
                font-size: 1rem;
            }
            
            .skill-card {
                padding: 20px;
            }
        }
        
        /* Horizontal Rule Styling */
        .divider {
            height: 4px;
            width: 80%;
            background: linear-gradient(to right, transparent, #6a11cb, transparent);
            margin: 40px auto;
            border-radius: 2px;
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <header>
        <div class="container header-content">
            <h1>Mahjabeen</h1>
            <div class="tagline">A passionate web designer</div>
            <a href="#projects" class="btn">View My Work</a>
        </div>
    </header>
    
    <!-- About Me Section -->
    <section class="section">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Hello! I'm Mahjabeen, a web designer.</p>
                    <p>I have a passion for creating clean, beautiful, and user-friendly websites. I specialize in HTML and CSS.</p>
                    <p>When I'm not coding, you can find me exploring new technologies, reading tech blogs, or hiking in the mountains.</p>
                    <p>Currently I'm a student of Intermediate and on the other hand I'm doing web development course in Saylani IT Park.</p>
                </div>
            </div>
        </div>
    </section>
    
    <div class="divider"></div>
    
    <!-- Skills Section -->
    <section class="section">
        <div class="container">
            <h2 class="section-title">My Skills</h2>
            <div class="skills-container">
                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fab fa-html5"></i>
                    </div>
                    <h3 class="skill-title">HTML5</h3>
                    <p class="skill-desc">Semantic markup and accessibility</p>
                </div>
                
                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fab fa-css3-alt"></i>
                    </div>
                    <h3 class="skill-title">CSS3</h3>
                    <p class="skill-desc">Responsive design and animations</p>
                </div>
                
                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fab fa-js"></i>
                    </div>
                    <h3 class="skill-title">JavaScript</h3>
                    <p class="skill-desc">Interactive and dynamic web experiences</p>
                </div>
            </div>
        </div>
    </section>
    
    <div class="divider"></div>
    
    <!-- Projects Section -->
    <section id="projects" class="section">
        <div class="container">
            <h2 class="section-title">My Projects</h2>
            <div class="projects-container">
                <div class="project-card">
                    <div class="project-placeholder">
                        <span>Portfolio Website</span>
                    </div>
                    <div class="project-info">
                        <h3 class="project-title">Personal Portfolio</h3>
                        <p class="project-desc">A responsive portfolio website built with HTML, CSS and JavaScript to showcase my work.</p>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-placeholder">
                        <span>E-commerce UI</span>
                    </div>
                    <div class="project-info">
                        <h3 class="project-title">Online Store Design</h3>
                        <p class="project-desc">A clean and modern e-commerce interface design with focus on user experience.</p>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-placeholder">
                        <span>Blog Template</span>
                    </div>
                    <div class="project-info">
                        <h3 class="project-title">Responsive Blog</h3>
                        <p class="project-desc">A fully responsive blog template with clean typography and mobile-friendly layout.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <div class="container">
            <p class="footer-text">© 2023 Mahjabeen. All rights reserved.</p>
            <p class="footer-text">Let's create something amazing together!</p>
            <div class="social-icons">
                <a href="#"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
            </div>
        </div>
    </footer>
    
    <script>
        // Simple script for smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Add animation on scroll
        const observerOptions = {
            threshold: 0.1
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if(entry.isIntersecting) {
                    entry.target.classList.add('animated');
                }
            });
        }, observerOptions);
        
        // Observe skill cards and project cards
        document.querySelectorAll('.skill-card, .project-card').forEach(card => {
            observer.observe(card);
        });
    </script>
</body>
</html>
