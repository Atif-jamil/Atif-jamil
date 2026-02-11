<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Atif Jamil - Portfolio</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            --primary: #0A66C2;
            --secondary: #1a1a2e;
            --accent: #4A90E2;
            --light: #f8f9fa;
            --dark: #121212;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, var(--dark) 0%, var(--secondary) 100%);
            color: var(--light);
            line-height: 1.6;
            padding: 20px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 30px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            animation: fadeIn 1s ease-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }
        
        @keyframes glow {
            0%, 100% { box-shadow: 0 0 20px var(--primary); }
            50% { box-shadow: 0 0 40px var(--accent); }
        }
        
        @keyframes slideIn {
            from { transform: translateX(-100px); opacity: 0; }
            to { transform: translateX(0); opacity: 1; }
        }
        
        header {
            text-align: center;
            padding: 40px 0;
        }
        
        .profile-img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            margin: 0 auto 30px;
            overflow: hidden;
            animation: float 6s ease-in-out infinite, glow 4s ease-in-out infinite;
            border: 4px solid var(--primary);
        }
        
        .profile-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        h1 {
            font-size: 3.5rem;
            background: linear-gradient(45deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 20px;
            animation: slideIn 1s ease-out;
        }
        
        .tagline {
            font-size: 1.5rem;
            color: #aaa;
            margin-bottom: 30px;
            animation: slideIn 1s ease-out 0.2s both;
        }
        
        .contact-badges {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin: 30px 0;
            animation: slideIn 1s ease-out 0.4s both;
        }
        
        .badge {
            padding: 12px 30px;
            background: linear-gradient(45deg, var(--primary), var(--accent));
            border-radius: 50px;
            text-decoration: none;
            color: white;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: all 0.3s ease;
        }
        
        .badge:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(74, 144, 226, 0.4);
        }
        
        .badge i {
            font-size: 1.2rem;
        }
        
        section {
            margin: 50px 0;
            padding: 40px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            animation: fadeIn 1s ease-out;
        }
        
        h2 {
            font-size: 2.2rem;
            margin-bottom: 30px;
            color: var(--accent);
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        h2 i {
            animation: spin 4s linear infinite;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }
        
        .skill-category {
            background: rgba(255, 255, 255, 0.08);
            padding: 25px;
            border-radius: 15px;
            transition: transform 0.3s ease;
        }
        
        .skill-category:hover {
            transform: translateY(-10px);
            background: rgba(74, 144, 226, 0.1);
        }
        
        .skill-icons {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
        }
        
        .icon {
            font-size: 2.5rem;
            transition: transform 0.3s ease;
        }
        
        .icon:hover {
            transform: scale(1.2);
        }
        
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }
        
        .stat-box {
            text-align: center;
            padding: 25px;
            background: rgba(255, 255, 255, 0.08);
            border-radius: 15px;
            transition: all 0.3s ease;
        }
        
        .stat-box:hover {
            transform: scale(1.05);
            background: rgba(74, 144, 226, 0.1);
        }
        
        .stat-number {
            font-size: 3rem;
            font-weight: 700;
            background: linear-gradient(45deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .quote {
            text-align: center;
            font-size: 1.8rem;
            font-style: italic;
            padding: 40px;
            margin: 50px 0;
            background: linear-gradient(45deg, rgba(10, 102, 194, 0.1), rgba(74, 144, 226, 0.1));
            border-radius: 15px;
            border-left: 5px solid var(--primary);
            animation: fadeIn 1s ease-out;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }
        
        .social-icon {
            font-size: 2rem;
            color: var(--light);
            transition: all 0.3s ease;
            padding: 10px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
        }
        
        .social-icon:hover {
            color: var(--accent);
            transform: translateY(-5px);
            background: rgba(74, 144, 226, 0.2);
        }
        
        @media (max-width: 768px) {
            h1 { font-size: 2.5rem; }
            .tagline { font-size: 1.2rem; }
            section { padding: 25px; }
            .contact-badges { flex-direction: column; align-items: center; }
            .badge { width: 100%; max-width: 300px; justify-content: center; }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.15.1/devicon.min.css">
</head>
<body>
    <div class="container">
        <header>
            <div class="profile-img">
                <img src="https://avatars.githubusercontent.com/u/your-github-id" alt="Atif Jamil">
            </div>
            <h1>Atif Jamil</h1>
            <div class="tagline">Frontend Engineer & React Specialist</div>
            
            <div class="contact-badges">
                <a href="https://www.linkedin.com/in/atif-jamil" class="badge">
                    <i class="fab fa-linkedin"></i> Professional Profile
                </a>
                <a href="mailto:atifjamil700@gmail.com" class="badge">
                    <i class="fas fa-envelope"></i> Contact Me
                </a>
                <a href="https://github.com/AtifJamil" class="badge">
                    <i class="fab fa-github"></i> GitHub Profile
                </a>
            </div>
        </header>

        <section style="animation-delay: 0.2s">
            <h2><i class="fas fa-user-tie"></i> Professional Summary</h2>
            <p style="font-size: 1.1rem; line-height: 1.8;">
                Frontend-focused Web Developer based in <strong>Lahore, Pakistan</strong>, specializing in building scalable, responsive, and performance-driven web applications. With a strong foundation in <strong>React, JavaScript, and modern UI architecture</strong>, I focus on writing clean, maintainable code and creating seamless user experiences. Currently advancing toward full-stack expertise through the <strong>MERN Stack ecosystem</strong>.
            </p>
        </section>

        <section style="animation-delay: 0.4s">
            <h2><i class="fas fa-code"></i> Technical Stack</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3><i class="fas fa-desktop"></i> Frontend</h3>
                    <div class="skill-icons">
                        <i class="devicon-html5-plain colored icon" title="HTML5"></i>
                        <i class="devicon-css3-plain colored icon" title="CSS3"></i>
                        <i class="devicon-javascript-plain colored icon" title="JavaScript"></i>
                        <i class="devicon-react-original colored icon" title="React"></i>
                        <i class="devicon-redux-original colored icon" title="Redux"></i>
                        <i class="devicon-tailwindcss-plain colored icon" title="Tailwind CSS"></i>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-server"></i> Backend & Database</h3>
                    <div class="skill-icons">
                        <i class="devicon-nodejs-plain colored icon" title="Node.js"></i>
                        <i class="devicon-express-original colored icon" title="Express"></i>
                        <i class="devicon-mongodb-plain colored icon" title="MongoDB"></i>
                        <i class="devicon-mysql-plain colored icon" title="MySQL"></i>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-tools"></i> Tools & Creative</h3>
                    <div class="skill-icons">
                        <i class="devicon-git-plain colored icon" title="Git"></i>
                        <i class="devicon-github-plain colored icon" title="GitHub"></i>
                        <i class="devicon-vscode-plain colored icon" title="VS Code"></i>
                        <i class="devicon-figma-plain colored icon" title="Figma"></i>
                        <i class="fas fa-paint-brush icon" style="color: #FF6B6B;" title="Canva"></i>
                        <i class="fas fa-video icon" style="color: #4ECDC4;" title="Premiere Pro"></i>
                    </div>
                </div>
            </div>
        </section>

        <section style="animation-delay: 0.6s">
            <h2><i class="fas fa-chart-line"></i> GitHub Analytics</h2>
            <div class="stats">
                <div class="stat-box">
                    <div class="stat-number" id="repos">50+</div>
                    <p>Repositories</p>
                </div>
                <div class="stat-box">
                    <div class="stat-number" id="commits">1000+</div>
                    <p>Commits</p>
                </div>
                <div class="stat-box">
                    <div class="stat-number" id="projects">20+</div>
                    <p>Projects</p>
                </div>
                <div class="stat-box">
                    <div class="stat-number" id="experience">2+</div>
                    <p>Years Experience</p>
                </div>
            </div>
        </section>

        <div class="quote">
            "Discipline in Code. Excellence in Execution."
        </div>

        <section style="animation-delay: 0.8s">
            <h2><i class="fas fa-handshake"></i> Let's Collaborate</h2>
            <p style="font-size: 1.1rem; margin-bottom: 20px;">
                I'm open to working on impactful frontend and full-stack projects. If you're building something meaningful — let's connect.
            </p>
            <div style="display: flex; flex-wrap: wrap; gap: 20px; margin-top: 30px;">
                <div style="flex: 1; min-width: 250px;">
                    <h3><i class="fas fa-envelope"></i> Email</h3>
                    <p>atifjamil700@gmail.com</p>
                </div>
                <div style="flex: 1; min-width: 250px;">
                    <h3><i class="fab fa-linkedin"></i> LinkedIn</h3>
                    <p>linkedin.com/in/atif-jamil</p>
                </div>
                <div style="flex: 1; min-width: 250px;">
                    <h3><i class="fas fa-map-marker-alt"></i> Location</h3>
                    <p>Lahore, Pakistan</p>
                </div>
            </div>
            
            <div class="social-links">
                <a href="https://github.com/AtifJamil" class="social-icon">
                    <i class="fab fa-github"></i>
                </a>
                <a href="https://twitter.com/yourusername" class="social-icon">
                    <i class="fab fa-twitter"></i>
                </a>
                <a href="https://stackoverflow.com/users/yourid" class="social-icon">
                    <i class="fab fa-stack-overflow"></i>
                </a>
                <a href="https://medium.com/@yourusername" class="social-icon">
                    <i class="fab fa-medium"></i>
                </a>
            </div>
        </section>
    </div>

    <script>
        // Animated counter for stats
        function animateCounter(element, target, duration = 2000) {
            let start = 0;
            const increment = target / (duration / 16);
            const timer = setInterval(() => {
                start += increment;
                if (start >= target) {
                    element.textContent = target + '+';
                    clearInterval(timer);
                } else {
                    element.textContent = Math.floor(start) + '+';
                }
            }, 16);
        }

        // Start animations when page loads
        document.addEventListener('DOMContentLoaded', () => {
            // Animate stats
            const stats = [
                { element: document.getElementById('repos'), target: 50 },
                { element: document.getElementById('commits'), target: 1000 },
                { element: document.getElementById('projects'), target: 20 },
                { element: document.getElementById('experience'), target: 2 }
            ];
            
            setTimeout(() => {
                stats.forEach(stat => {
                    if (stat.element) {
                        animateCounter(stat.element, stat.target);
                    }
                });
            }, 1000);

            // Add hover effect to skill icons
            document.querySelectorAll('.icon').forEach(icon => {
                icon.addEventListener('mouseenter', function() {
                    this.style.transform = 'scale(1.3) rotate(5deg)';
                });
                icon.addEventListener('mouseleave', function() {
                    this.style.transform = 'scale(1) rotate(0deg)';
                });
            });
        });
    </script>
</body>
</html>
