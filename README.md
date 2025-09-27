<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DSA Master - Portfolio</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: #333;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header Section */
        header {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            text-align: center;
            margin-bottom: 30px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid rgba(255, 255, 255, 0.3);
            margin-bottom: 20px;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
            color: white;
            margin-left: auto;
            margin-right: auto;
        }

        .typing-text {
            font-size: 2.5rem;
            font-weight: bold;
            color: white;
            margin-bottom: 10px;
        }

        .subtitle {
            font-size: 1.2rem;
            color: rgba(255, 255, 255, 0.8);
            margin-bottom: 30px;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }

        .social-links a {
            color: white;
            font-size: 1.5rem;
            padding: 10px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            transition: all 0.3s ease;
            text-decoration: none;
        }

        .social-links a:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: translateY(-3px);
        }

        /* Stats Section */
        .stats-section {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .stat-card {
            background: rgba(255, 255, 255, 0.95);
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .stat-card:hover {
            transform: translateY(-5px);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: #667eea;
            margin-bottom: 10px;
        }

        .stat-label {
            font-size: 1rem;
            color: #666;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .platform-icon {
            font-size: 2rem;
            margin-bottom: 15px;
            color: #764ba2;
        }

        /* Skills Section */
        .skills-section {
            background: rgba(255, 255, 255, 0.95);
            padding: 40px;
            border-radius: 20px;
            margin-bottom: 30px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
        }

        .section-title {
            font-size: 2rem;
            text-align: center;
            margin-bottom: 30px;
            color: #333;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .skill-category {
            background: #f8f9fa;
            padding: 25px;
            border-radius: 15px;
            border-left: 5px solid #667eea;
        }

        .skill-category h3 {
            color: #333;
            margin-bottom: 20px;
            font-size: 1.3rem;
        }

        .skill-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }

        .skill-name {
            font-weight: 500;
            color: #555;
        }

        .skill-bar {
            width: 60%;
            height: 8px;
            background: #e0e0e0;
            border-radius: 10px;
            overflow: hidden;
        }

        .skill-progress {
            height: 100%;
            background: linear-gradient(90deg, #667eea, #764ba2);
            border-radius: 10px;
            animation: fillBar 2s ease-in-out;
        }

        @keyframes fillBar {
            from { width: 0%; }
            to { width: 100%; }
        }

        /* Projects Section */
        .projects-section {
            background: rgba(255, 255, 255, 0.95);
            padding: 40px;
            border-radius: 20px;
            margin-bottom: 30px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 25px;
        }

        .project-card {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            padding: 30px;
            border-radius: 15px;
            color: white;
            position: relative;
            overflow: hidden;
            transition: transform 0.3s ease;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(255, 255, 255, 0.1);
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
        }

        .project-card:hover::before {
            opacity: 1;
        }

        .project-title {
            font-size: 1.4rem;
            margin-bottom: 15px;
            position: relative;
            z-index: 2;
        }

        .project-description {
            margin-bottom: 20px;
            opacity: 0.9;
            position: relative;
            z-index: 2;
        }

        .project-stats {
            display: flex;
            justify-content: space-between;
            font-size: 0.9rem;
            position: relative;
            z-index: 2;
        }

        /* Progress Tracker */
        .progress-section {
            background: rgba(255, 255, 255, 0.95);
            padding: 40px;
            border-radius: 20px;
            margin-bottom: 30px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
        }

        .progress-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px;
            margin-bottom: 15px;
            background: #f8f9fa;
            border-radius: 10px;
            transition: all 0.3s ease;
        }

        .progress-item:hover {
            background: #e9ecef;
            transform: translateX(5px);
        }

        .progress-info h4 {
            color: #333;
            margin-bottom: 5px;
        }

        .progress-info p {
            color: #666;
            font-size: 0.9rem;
        }

        .progress-circle {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background: conic-gradient(#667eea 0deg, #764ba2 180deg, #e0e0e0 180deg);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .container {
                padding: 10px;
            }

            .typing-text {
                font-size: 2rem;
            }

            .stats-section {
                grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            }

            .skills-grid, .projects-grid {
                grid-template-columns: 1fr;
            }

            header {
                padding: 20px;
            }
        }

        /* Animation Classes */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            animation: fadeIn 0.8s ease-out forwards;
        }

        @keyframes fadeIn {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .bounce {
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateY(0);
            }
            40% {
                transform: translateY(-10px);
            }
            60% {
                transform: translateY(-5px);
            }
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
        }

        ::-webkit-scrollbar-thumb {
            background: linear-gradient(135deg, #667eea, #764ba2);
            border-radius: 10px;
        }

        /* Floating Elements */
        .floating {
            animation: floating 3s ease-in-out infinite;
        }

        @keyframes floating {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <header class="fade-in">
            <div class="profile-img floating">
                <i class="fas fa-code"></i>
            </div>
            <div class="typing-text" id="typing-text">DSA Master</div>
            <div class="subtitle">Problem Solving Enthusiast | Competitive Programmer</div>
            <div class="social-links">
                <a href="https://github.com/yourusername" title="GitHub"><i class="fab fa-github"></i></a>
                <a href="https://leetcode.com/yourusername" title="LeetCode"><i class="fas fa-code"></i></a>
                <a href="https://linkedin.com/in/yourusername" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
                <a href="https://codeforces.com/profile/yourusername" title="Codeforces"><i class="fas fa-trophy"></i></a>
            </div>
        </header>

        <!-- Stats Section -->
        <div class="stats-section">
            <div class="stat-card fade-in" style="animation-delay: 0.2s;">
                <div class="platform-icon"><i class="fas fa-code"></i></div>
                <div class="stat-number" data-target="500">0</div>
                <div class="stat-label">LeetCode Problems</div>
            </div>
            <div class="stat-card fade-in" style="animation-delay: 0.4s;">
                <div class="platform-icon"><i class="fas fa-trophy"></i></div>
                <div class="stat-number" data-target="300">0</div>
                <div class="stat-label">HackerRank Problems</div>
            </div>
            <div class="stat-card fade-in" style="animation-delay: 0.6s;">
                <div class="platform-icon"><i class="fas fa-star"></i></div>
                <div class="stat-number" data-target="1547">0</div>
                <div class="stat-label">Codeforces Rating</div>
            </div>
            <div class="stat-card fade-in" style="animation-delay: 0.8s;">
                <div class="platform-icon"><i class="fas fa-fire"></i></div>
                <div class="stat-number" data-target="150">0</div>
                <div class="stat-label">Day Streak</div>
            </div>
        </div>

        <!-- Skills Section -->
        <div class="skills-section fade-in">
            <h2 class="section-title">Technical Skills</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3><i class="fas fa-laptop-code"></i> Programming Languages</h3>
                    <div class="skill-item">
                        <span class="skill-name">C++</span>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 95%;"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <span class="skill-name">Python</span>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 85%;"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <span class="skill-name">Java</span>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 80%;"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <span class="skill-name">JavaScript</span>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 75%;"></div>
                        </div>
                    </div>
                </div>

                <div class="skill-category">
                    <h3><i class="fas fa-brain"></i> Algorithm Topics</h3>
                    <div class="skill-item">
                        <span class="skill-name">Dynamic Programming</span>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 90%;"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <span class="skill-name">Graph Algorithms</span>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 85%;"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <span class="skill-name">Tree Algorithms</span>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 88%;"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <span class="skill-name">Greedy Algorithms</span>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 82%;"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Projects Section -->
        <div class="projects-section fade-in">
            <h2 class="section-title">Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-title">
                        <i class="fas fa-sitemap"></i> DSA Visualizer
                    </div>
                    <div class="project-description">
                        Interactive web application to visualize sorting algorithms, graph traversals, and data structures with step-by-step animations.
                    </div>
                    <div class="project-stats">
                        <span><i class="fas fa-star"></i> 127 stars</span>
                        <span><i class="fas fa-code-branch"></i> 23 forks</span>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-title">
                        <i class="fas fa-robot"></i> LeetCode Auto-Submitter
                    </div>
                    <div class="project-description">
                        Python automation tool that fetches daily LeetCode problems, generates template solutions, and tracks progress with statistics.
                    </div>
                    <div class="project-stats">
                        <span><i class="fas fa-star"></i> 89 stars</span>
                        <span><i class="fas fa-download"></i> 234 downloads</span>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-title">
                        <i class="fas fa-chart-line"></i> Algorithm Complexity Analyzer
                    </div>
                    <div class="project-description">
                        Tool that analyzes code complexity, provides optimization suggestions, and compares different algorithmic approaches.
                    </div>
                    <div class="project-stats">
                        <span><i class="fas fa-star"></i> 156 stars</span>
                        <span><i class="fas fa-eye"></i> 1.2k views</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Progress Tracker -->
        <div class="progress-section fade-in">
            <h2 class="section-title">Current Learning Progress</h2>
            
            <div class="progress-item">
                <div class="progress-info">
                    <h4>Advanced Dynamic Programming</h4>
                    <p>Mastering optimization problems and state-space reduction techniques</p>
                </div>
                <div class="progress-circle">85%</div>
            </div>

            <div class="progress-item">
                <div class="progress-info">
                    <h4>System Design Fundamentals</h4>
                    <p>Learning scalable architecture patterns and distributed systems</p>
                </div>
                <div class="progress-circle">60%</div>
            </div>

            <div class="progress-item">
                <div class="progress-info">
                    <h4>Competitive Programming</h4>
                    <p>Participating in contests and improving problem-solving speed</p>
                </div>
                <div class="progress-circle">75%</div>
            </div>

            <div class="progress-item">
                <div class="progress-info">
                    <h4>Advanced Graph Algorithms</h4>
                    <p>Network flows, minimum cuts, and advanced shortest path algorithms</p>
                </div>
                <div class="progress-circle">70%</div>
            </div>
        </div>
    </div>

    <script>
        // Typing animation
        const texts = ['DSA Master', 'Problem Solver', 'Code Optimizer', 'Algorithm Expert'];
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        const typingElement = document.getElementById('typing-text');

        function typeText() {
            const currentText = texts[textIndex];
            
            if (isDeleting) {
                typingElement.textContent = currentText.substring(0, charIndex - 1);
                charIndex--;
            } else {
                typingElement.textContent = currentText.substring(0, charIndex + 1);
                charIndex++;
            }

            if (!isDeleting && charIndex === currentText.length) {
                setTimeout(() => isDeleting = true, 2000);
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                textIndex = (textIndex + 1) % texts.length;
            }

            const speed = isDeleting ? 50 : 100;
            setTimeout(typeText, speed);
        }

        // Counter animation
        function animateCounters() {
            const counters = document.querySelectorAll('.stat-number');
            counters.forEach(counter => {
                const target = parseInt(counter.getAttribute('data-target'));
                const increment = target / 100;
                let current = 0;

                const updateCounter = () => {
                    if (current < target) {
                        current += increment;
                        counter.textContent = Math.ceil(current);
                        setTimeout(updateCounter, 20);
                    } else {
                        counter.textContent = target;
                    }
                };

                updateCounter();
            });
        }

        // Intersection Observer for animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animationDelay = '0s';
                    entry.target.classList.add('fade-in');
                    
                    if (entry.target.classList.contains('stats-section')) {
                        setTimeout(animateCounters, 500);
                    }
                }
            });
        }, observerOptions);

        // Observe all sections
        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });

        // Initialize
        document.addEventListener('DOMContentLoaded', () => {
            typeText();
        });

        // Smooth scrolling for any internal links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Add hover effects to project cards
        document.querySelectorAll('.project-card').forEach(card => {
            card.addEventListener('mouseenter', function() {
                this.style.transform = 'translateY(-5px) scale(1.02)';
            });
            
            card.addEventListener('mouseleave', function() {
                this.style.transform = 'translateY(0) scale(1)';
            });
        });

        // Random floating animation delays
        document.querySelectorAll('.floating').forEach((el, index) => {
            el.style.animationDelay = `${index * 0.5}s`;
        });
    </script>
</body>
</html>
