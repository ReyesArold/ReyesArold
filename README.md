<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arold Reyes - Developer Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
            color: #e2e8f0;
            min-height: 100vh;
            padding: 40px 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .header {
            text-align: center;
            margin-bottom: 60px;
            padding: 40px;
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .header h1 {
            font-size: 3.5em;
            margin-bottom: 10px;
            background: linear-gradient(135deg, #6366f1 0%, #a855f7 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .header .tagline {
            font-size: 1.3em;
            color: #94a3b8;
            margin-bottom: 20px;
        }

        .wave {
            display: inline-block;
            animation: wave 2s infinite;
            font-size: 1.5em;
        }

        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(20deg); }
            75% { transform: rotate(-20deg); }
        }

        .typing-text {
            font-size: 1.2em;
            color: #6366f1;
            margin-top: 15px;
            font-weight: 600;
        }

        .section {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 30px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .section h2 {
            font-size: 2em;
            margin-bottom: 20px;
            color: #6366f1;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .about-code {
            background: #1e293b;
            border-left: 4px solid #6366f1;
            padding: 20px;
            border-radius: 10px;
            font-family: 'Courier New', monospace;
            color: #94a3b8;
            line-height: 1.8;
            overflow-x: auto;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .tech-item {
            background: rgba(99, 102, 241, 0.1);
            padding: 25px;
            border-radius: 15px;
            text-align: center;
            border: 2px solid rgba(99, 102, 241, 0.3);
            transition: all 0.3s ease;
        }

        .tech-item:hover {
            transform: translateY(-5px);
            border-color: #6366f1;
            box-shadow: 0 10px 30px rgba(99, 102, 241, 0.3);
        }

        .tech-icon {
            font-size: 3em;
            margin-bottom: 10px;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .stat-card {
            background: linear-gradient(135deg, rgba(99, 102, 241, 0.1) 0%, rgba(168, 85, 247, 0.1) 100%);
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            border: 1px solid rgba(99, 102, 241, 0.3);
        }

        .stat-number {
            font-size: 3em;
            font-weight: bold;
            background: linear-gradient(135deg, #6366f1 0%, #a855f7 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .stat-label {
            color: #94a3b8;
            margin-top: 10px;
            font-size: 1.1em;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-top: 20px;
        }

        .project-card {
            background: rgba(30, 41, 59, 0.8);
            padding: 30px;
            border-radius: 15px;
            border: 1px solid rgba(99, 102, 241, 0.3);
            transition: all 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
            border-color: #6366f1;
            box-shadow: 0 15px 40px rgba(99, 102, 241, 0.2);
        }

        .project-card h3 {
            color: #6366f1;
            margin-bottom: 15px;
            font-size: 1.5em;
        }

        .project-card p {
            color: #94a3b8;
            line-height: 1.6;
            margin-bottom: 15px;
        }

        .project-link {
            display: inline-block;
            color: #6366f1;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .project-link:hover {
            color: #a855f7;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
            flex-wrap: wrap;
        }

        .social-btn {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            padding: 15px 30px;
            background: linear-gradient(135deg, #6366f1 0%, #a855f7 100%);
            color: white;
            text-decoration: none;
            border-radius: 10px;
            font-weight: 600;
            transition: all 0.3s ease;
            border: none;
        }

        .social-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(99, 102, 241, 0.4);
        }

        .quote-section {
            text-align: center;
            font-style: italic;
            color: #94a3b8;
            font-size: 1.2em;
            padding: 30px;
            background: rgba(99, 102, 241, 0.05);
            border-radius: 15px;
            margin-top: 30px;
        }

        .footer {
            text-align: center;
            margin-top: 50px;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #64748b;
        }

        @media (max-width: 768px) {
            .header h1 {
                font-size: 2.5em;
            }
            
            .section {
                padding: 25px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>Arold Reyes <span class="wave">👋</span></h1>
            <div class="tagline">Full Stack Developer | Creative Coder | Tech Enthusiast</div>
            <div class="typing-text">🚀 Building amazing projects ✨</div>
        </div>

        <div class="section">
            <h2>🌟 About Me</h2>
            <div class="about-code">
const arold = {<br>
&nbsp;&nbsp;&nbsp;&nbsp;location: "Manila, Philippines 🇵🇭",<br>
&nbsp;&nbsp;&nbsp;&nbsp;code: ["HTML", "CSS", "JavaScript", "Python"],<br>
&nbsp;&nbsp;&nbsp;&nbsp;currentFocus: "Web Development & Design",<br>
&nbsp;&nbsp;&nbsp;&nbsp;funFact: "I debug with console.log() 🐛",<br>
&nbsp;&nbsp;&nbsp;&nbsp;passion: "Creating beautiful web experiences"<br>
};
            </div>
        </div>

        <div class="section">
            <h2>🚀 Tech Stack</h2>
            <div class="tech-grid">
                <div class="tech-item">
                    <div class="tech-icon">🌐</div>
                    <div>HTML5</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🎨</div>
                    <div>CSS3</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">⚡</div>
                    <div>JavaScript</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🔧</div>
                    <div>Git</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">💻</div>
                    <div>VS Code</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🐙</div>
                    <div>GitHub</div>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>📊 GitHub Stats</h2>
            <div class="stats-grid">
                <div class="stat-card">
                    <div class="stat-number">32</div>
                    <div class="stat-label">Contributions</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">4</div>
                    <div class="stat-label">Repositories</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">28</div>
                    <div class="stat-label">Commits</div>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>📌 Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <h3>🔥 blaze.github.io</h3>
                    <p>A modern and responsive website showcasing creative web development skills and innovative design patterns.</p>
                    <a href="https://github.com/Arold-Reyes/blaze.github.io" class="project-link">View Project →</a>
                </div>
                <div class="project-card">
                    <h3>👨‍💻 Arold-Reyes</h3>
                    <p>Personal GitHub profile repository featuring a dynamic README with stats, skills, and project highlights.</p>
                    <a href="https://github.com/Arold-Reyes/Arold-Reyes" class="project-link">View Project →</a>
                </div>
                <div class="project-card">
                    <h3>🎮 noobgamingph</h3>
                    <p>An exciting gaming-related project showcasing interactive elements and engaging user experience design.</p>
                    <a href="https://github.com/Arold-Reyes/noobgamingph" class="project-link">View Project →</a>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>📫 Let's Connect</h2>
            <div class="social-links">
                <a href="https://facebook.com/reyes.arold.92" class="social-btn">
                    📘 Facebook
                </a>
                <a href="https://github.com/Arold-Reyes" class="social-btn">
                    🐙 GitHub
                </a>
            </div>
        </div>

        <div class="quote-section">
            💬 "Code is like humor. When you have to explain it, it's bad." – Cory House
        </div>

        <div class="footer">
            <p>Made with ❤️ by Arold Reyes</p>
            <p>© 2025 - Keep Coding, Keep Creating</p>
        </div>
    </div>
</body>
</html>
