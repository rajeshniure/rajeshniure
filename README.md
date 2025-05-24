<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rajesh Niure - GitHub Profile</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600;700&family=Inter:wght@300;400;500;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: white;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
        }
        
        /* Animated background particles */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        
        .particle {
            position: absolute;
            width: 4px;
            height: 4px;
            background: rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); opacity: 0.3; }
            50% { transform: translateY(-20px) rotate(180deg); opacity: 0.8; }
        }
        
        /* Header section with typing animation */
        .header {
            text-align: center;
            margin-bottom: 60px;
            position: relative;
        }
        
        .header h1 {
            font-size: 4rem;
            font-weight: 700;
            margin-bottom: 20px;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45b7d1, #f9ca24);
            background-size: 400% 400%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradientShift 3s ease-in-out infinite;
        }
        
        @keyframes gradientShift {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }
        
        .typing-container {
            display: inline-block;
            position: relative;
        }
        
        .typing-text {
            font-size: 1.5rem;
            font-weight: 500;
            color: rgba(255, 255, 255, 0.9);
            border-right: 3px solid #4ecdc4;
            animation: typing 3s steps(40) infinite, blink 1s infinite;
        }
        
        @keyframes typing {
            0%, 50% { width: 0; }
            100% { width: 100%; }
        }
        
        @keyframes blink {
            0%, 50% { border-color: transparent; }
            51%, 100% { border-color: #4ecdc4; }
        }
        
        /* Profile card with glassmorphism */
        .profile-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(20px);
            border-radius: 25px;
            padding: 40px;
            margin-bottom: 40px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            animation: slideInUp 1s ease-out;
        }
        
        @keyframes slideInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .profile-info {
            display: grid;
            grid-template-columns: 1fr 300px;
            gap: 40px;
            align-items: center;
        }
        
        .info-text {
            font-size: 1.1rem;
            line-height: 1.8;
        }
        
        .info-item {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
            padding: 15px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            transition: all 0.3s ease;
        }
        
        .info-item:hover {
            background: rgba(255, 255, 255, 0.1);
            transform: translateX(10px);
        }
        
        .info-icon {
            width: 24px;
            height: 24px;
            margin-right: 15px;
            color: #4ecdc4;
        }
        
        .coding-gif {
            width: 100%;
            border-radius: 20px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
            animation: pulse 3s ease-in-out infinite;
        }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }
        
        /* Social links with hover effects */
        .social-section {
            margin: 50px 0;
            text-align: center;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 30px;
        }
        
        .social-link {
            width: 60px;
            height: 60px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            color: white;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .social-link::before {
            content: '';
            position: absolute;
            width: 0;
            height: 100%;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            transition: width 0.3s ease;
            z-index: -1;
        }
        
        .social-link:hover {
            transform: translateY(-10px) scale(1.1);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
        }
        
        .social-link:hover::before {
            width: 100%;
        }
        
        /* Tech stack with animated icons */
        .tech-section {
            margin: 50px 0;
        }
        
        .section-title {
            font-size: 2.5rem;
            font-weight: 700;
            text-align: center;
            margin-bottom: 40px;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            border-radius: 2px;
        }
        
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(80px, 1fr));
            gap: 30px;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .tech-item {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 20px;
            text-align: center;
            transition: all 0.3s ease;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }
        
        .tech-item::before {
            content: '';
            position: absolute;
            top: -100%;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, rgba(255, 107, 107, 0.3), rgba(78, 205, 196, 0.3));
            transition: top 0.3s ease;
            z-index: -1;
        }
        
        .tech-item:hover {
            transform: translateY(-15px) rotateY(10deg);
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.3);
        }
        
        .tech-item:hover::before {
            top: 0;
        }
        
        .tech-icon {
            width: 50px;
            height: 50px;
            margin-bottom: 10px;
            animation: spin 10s linear infinite;
        }
        
        @keyframes spin {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        
        .tech-name {
            font-size: 0.9rem;
            font-weight: 500;
            color: rgba(255, 255, 255, 0.9);
        }
        
        /* Stats section with animated counters */
        .stats-section {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 50px 0;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(20px);
            border-radius: 20px;
            padding: 30px;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: all 0.3s ease;
        }
        
        .stat-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.2);
        }
        
        .stat-card img {
            width: 100%;
            border-radius: 15px;
            transition: all 0.3s ease;
        }
        
        .stat-card:hover img {
            transform: scale(1.05);
        }
        
        /* Responsive design */
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2.5rem;
            }
            
            .profile-info {
                grid-template-columns: 1fr;
                text-align: center;
            }
            
            .social-links {
                flex-wrap: wrap;
                gap: 20px;
            }
            
            .tech-grid {
                grid-template-columns: repeat(auto-fit, minmax(60px, 1fr));
                gap: 20px;
            }
        }
        
        /* Profile views counter */
        .profile-views {
            display: inline-block;
            background: rgba(255, 255, 255, 0.1);
            padding: 10px 20px;
            border-radius: 25px;
            margin-top: 20px;
            animation: bounce 2s ease-in-out infinite;
        }
        
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-10px); }
            60% { transform: translateY(-5px); }
        }
    </style>
</head>
<body>
    <!-- Animated background particles -->
    <div class="particles" id="particles"></div>
    
    <div class="container">
        <!-- Header Section -->
        <div class="header">
            <h1>Hi 👋, I'm Rajesh Niure</h1>
            <div class="typing-container">
                <div class="typing-text">Passionate about backend development with Django and Python</div>
            </div>
            <div class="profile-views">
                <img src="https://komarev.com/ghpvc/?username=rajeshniure&label=Profile%20views&color=4ecdc4&style=for-the-badge" alt="Profile Views">
            </div>
        </div>
        
        <!-- Profile Card -->
        <div class="profile-card">
            <div class="profile-info">
                <div class="info-text">
                    <div class="info-item">
                        <svg class="info-icon" fill="currentColor" viewBox="0 0 20 20">
                            <path d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/>
                        </svg>
                        <span>🔭 I'm currently working on <strong>Django Project</strong></span>
                    </div>
                    <div class="info-item">
                        <svg class="info-icon" fill="currentColor" viewBox="0 0 20 20">
                            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                        </svg>
                        <span>🌱 I'm currently learning <strong>React, AWS</strong></span>
                    </div>
                    <div class="info-item">
                        <svg class="info-icon" fill="currentColor" viewBox="0 0 20 20">
                            <path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"/>
                            <path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"/>
                        </svg>
                        <span>📫 How to reach me: <strong>rajeshniure567@gmail.com</strong></span>
                    </div>
                    <div class="info-item">
                        <svg class="info-icon" fill="currentColor" viewBox="0 0 20 20">
                            <path fill-rule="evenodd" d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-7-4a1 1 0 11-2 0 1 1 0 012 0zM9 9a1 1 0 000 2v3a1 1 0 001 1h1a1 1 0 100-2v-3a1 1 0 00-1-1H9z" clip-rule="evenodd"/>
                        </svg>
                        <span>⚡ Fun fact: <strong>I write better code after a guitar solo</strong></span>
                    </div>
                </div>
                <div>
                    <img src="https://raw.githubusercontent.com/chiraag-kakar/chiraag-kakar/master/hadder.gif" 
                         alt="Coding" class="coding-gif">
                </div>
            </div>
        </div>
        
        <!-- Social Links -->
        <div class="social-section">
            <h2 class="section-title">Connect with me</h2>
            <div class="social-links">
                <a href="https://linkedin.com/in/rajeshniure" class="social-link" title="LinkedIn">
                    <svg width="24" height="24" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                    </svg>
                </a>
                <a href="https://www.facebook.com/rajesh.niure.7" class="social-link" title="Facebook">
                    <svg width="24" height="24" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/>
                    </svg>
                </a>
                <a href="https://instagram.com/raj_niure" class="social-link" title="Instagram">
                    <svg width="24" height="24" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                    </svg>
                </a>
            </div>
        </div>
        
        <!-- Tech Stack -->
        <div class="tech-section">
            <h2 class="section-title">Languages and Tools</h2>
            <div class="tech-grid">
                <div class="tech-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="Python" class="tech-icon">
                    <div class="tech-name">Python</div>
                </div>
                <div class="tech-item">
                    <img src="https://cdn.worldvectorlogo.com/logos/django.svg" alt="Django" class="tech-icon">
                    <div class="tech-name">Django</div>
                </div>
                <div class="tech-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="JavaScript" class="tech-icon">
                    <div class="tech-name">JavaScript</div>
                </div>
                <div class="tech-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg" alt="React" class="tech-icon">
                    <div class="tech-name">React</div>
                </div>
                <div class="tech-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="HTML5" class="tech-icon">
                    <div class="tech-name">HTML5</div>
                </div>
                <div class="tech-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="CSS3" class="tech-icon">
                    <div class="tech-name">CSS3</div>
                </div>
                <div class="tech-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="MySQL" class="tech-icon">
                    <div class="tech-name">MySQL</div>
                </div>
                <div class="tech-item">
                    <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="Git" class="tech-icon">
                    <div class="tech-name">Git</div>
                </div>
                <div class="tech-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="Linux" class="tech-icon">
                    <div class="tech-name">Linux</div>
                </div>
                <div class="tech-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" alt="C" class="tech-icon">
                    <div class="tech-name">C</div>
                </div>
                <div class="tech-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" alt="C++" class="tech-icon">
                    <div class="tech-name">C++</div>
                </div>
                <div class="tech-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg" alt="PHP" class="tech-icon">
                    <div class="tech-name">PHP</div>
                </div>
            </div>
        </div>
        
        <!-- GitHub Stats -->
        <div class="stats-section">
            <div class="stat-card">
                <img src="https://github-readme-stats.vercel.app/api/top-langs?username=rajeshniure&show_icons=true&locale=en&layout=compact&theme=radical" alt="Top Languages">
            </div>
            <div class="stat-card">
                <img src="https://github-readme-stats.vercel.app/api?username=rajeshniure&show_icons=true&locale=en&theme=radical" alt="GitHub Stats">
            </div>
            <div class="stat-card">
                <img src="https://github-readme-streak-stats.herokuapp.com/?user=rajeshniure&theme=radical" alt="GitHub Streak">
            </div>
        </div>
    </div>
    
    <script>
        // Create animated particles
        function createParticles() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = 50;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.top = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 6 + 's';
                particle.style.animationDuration = (Math.random() * 3 + 3) + 's';
                particlesContainer.appendChild(particle);
            }
        }
        
        // Typing animation
        function typeWriter() {
            const text = "Passionate about backend development with Django and Python";
            const element = document.querySelector('.typing-text');
            element.innerHTML = '';
            element.style.width = '0';
            
            let i = 0;
            const timer = setInterval(function() {
                if (i < text.length) {
                    element.innerHTML += text.charAt(i);
                    i++;
                } else {
                    clearInterval(timer);
                    setTimeout(() => {
                        element.style.width = '0';
                        setTimeout(typeWriter, 1000);
                    }, 3000);
                }
            }, 100);
        }
        
        // Initialize animations
        document.addEventListener('DOMContentLoaded', function() {
            createParticles();
            typeWriter();
            
            // Add scroll animations
            const observerOptions = {
                threshold: 0.1,
                rootMargin: '0px 0px -50px 0px'
            };
            
            const observer = new IntersectionObserver(function(entries) {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.animationPlayState = 'running';
                    }
                });
            }, observerOptions);
            
            // Observe tech items for staggered animations
            document.querySelectorAll('.tech-item').forEach((item, index) => {
                item.style.animationDelay = (index * 0.1) + 's';
                observer.observe(item);
            });
            
            // Add hover sound effects (optional)
            document.querySelectorAll('.social-link, .tech-item').forEach(item => {
                item.addEventListener('mouseenter', function() {
                    this.style.transform += ' scale(1.05)';
                });
                
                item.addEventListener('mouseleave', function() {
                    this.style.transform = this.style.transform.replace(' scale(1.05)', '');
                });
            });
        });
    </script>
</body>
</html>
