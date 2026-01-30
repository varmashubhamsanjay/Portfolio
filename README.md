<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shubham Sanjay Varma | Founder & AI Expert</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;500;700&display=swap" rel="stylesheet">
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        /* --- 1. PROFESSIONAL DESIGN SYSTEM --- */
        :root {
            --bg-color: #050505;
            --text-primary: #ffffff;
            --text-secondary: #a1a1aa;
            --accent-purple: #8b5cf6; /* Modern Violet */
            --accent-glow: rgba(139, 92, 246, 0.5);
            --glass-bg: rgba(255, 255, 255, 0.03);
            --glass-border: rgba(255, 255, 255, 0.06);
            --card-hover: rgba(255, 255, 255, 0.08);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-primary);
            font-family: 'Outfit', sans-serif;
            overflow-x: hidden;
            line-height: 1.6;
        }

        /* --- 2. AMBIENT BACKGROUND GLOW (Aurora Effect) --- */
        .glow-blob {
            position: fixed;
            top: -20%;
            left: -10%;
            width: 50vw;
            height: 50vw;
            background: radial-gradient(circle, var(--accent-glow) 0%, transparent 70%);
            opacity: 0.4;
            filter: blur(80px);
            z-index: -1;
            animation: float 10s ease-in-out infinite alternate;
        }
        
        .glow-blob:nth-child(2) {
            top: auto;
            bottom: -20%;
            left: auto;
            right: -10%;
            animation-delay: -5s;
        }

        @keyframes float {
            0% { transform: translate(0, 0); }
            100% { transform: translate(30px, 50px); }
        }

        /* --- 3. NAVIGATION --- */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 20px 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: rgba(5, 5, 5, 0.8);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid var(--glass-border);
            z-index: 1000;
        }

        .brand {
            font-size: 1.25rem;
            font-weight: 700;
            letter-spacing: -0.5px;
            color: #fff;
        }
        
        .brand span { color: var(--accent-purple); }

        .nav-links { display: flex; gap: 40px; }

        .nav-links a {
            text-decoration: none;
            color: var(--text-secondary);
            font-size: 0.95rem;
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover { color: #fff; }

        /* --- 4. HERO SECTION --- */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 120px 10% 80px;
            gap: 60px;
        }

        .hero-content { flex: 1; }

        .pill {
            display: inline-flex;
            align-items: center;
            padding: 6px 16px;
            background: rgba(139, 92, 246, 0.1);
            border: 1px solid rgba(139, 92, 246, 0.2);
            border-radius: 99px;
            color: var(--accent-purple);
            font-size: 0.85rem;
            font-weight: 600;
            margin-bottom: 24px;
        }

        h1 {
            font-size: 3.5rem;
            line-height: 1.1;
            font-weight: 700;
            margin-bottom: 20px;
            letter-spacing: -1px;
        }

        h1 span {
            background: linear-gradient(to right, #fff, #a78bfa);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .subtitle {
            font-size: 1.125rem;
            color: var(--text-secondary);
            max-width: 500px;
            margin-bottom: 32px;
        }

        .btn-group { display: flex; gap: 16px; }

        .btn {
            padding: 12px 28px;
            border-radius: 8px;
            font-weight: 500;
            text-decoration: none;
            transition: all 0.3s ease;
            font-size: 0.95rem;
        }

        .btn-primary {
            background: var(--accent-purple);
            color: #fff;
            box-shadow: 0 4px 20px rgba(139, 92, 246, 0.3);
        }

        .btn-primary:hover {
            background: #7c3aed;
            transform: translateY(-2px);
        }

        .btn-secondary {
            background: rgba(255, 255, 255, 0.05);
            color: #fff;
            border: 1px solid var(--glass-border);
        }

        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.1);
        }

        /* --- HERO IMAGE --- */
        .image-wrapper {
            position: relative;
            width: 380px;
            height: 380px;
            border-radius: 24px;
            overflow: hidden;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5);
        }
        
        .profile-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .image-wrapper:hover .profile-img {
            transform: scale(1.05);
        }

        /* --- 5. SECTIONS --- */
        section { padding: 100px 10%; }

        .section-header { margin-bottom: 60px; }
        
        .section-title {
            font-size: 2rem;
            margin-bottom: 12px;
        }
        
        .section-desc {
            color: var(--text-secondary);
            font-size: 1rem;
        }

        /* --- 6. GRID LAYOUTS --- */
        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
        }

        /* --- 7. CARDS (Glassmorphism) --- */
        .card {
            background: var(--glass-bg);
            border: 1px solid var(--glass-border);
            padding: 32px;
            border-radius: 16px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .card:hover {
            background: var(--card-hover);
            transform: translateY(-5px);
            border-color: rgba(139, 92, 246, 0.3);
        }

        .card-icon {
            width: 48px;
            height: 48px;
            background: rgba(139, 92, 246, 0.1);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--accent-purple);
            font-size: 1.25rem;
            margin-bottom: 24px;
        }

        .card h3 {
            font-size: 1.25rem;
            margin-bottom: 12px;
        }

        .card p {
            color: var(--text-secondary);
            font-size: 0.95rem;
            margin-bottom: 24px;
        }

        .tags { display: flex; gap: 8px; flex-wrap: wrap; }

        .tag {
            font-size: 0.75rem;
            padding: 4px 10px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 6px;
            color: #ccc;
        }

        /* --- 8. EDUCATION --- */
        .edu-card {
            display: flex;
            align-items: center;
            gap: 20px;
            background: linear-gradient(90deg, var(--glass-bg) 0%, transparent 100%);
            padding: 40px;
            border-left: 4px solid var(--accent-purple);
            border-radius: 0 16px 16px 0;
        }
        
        .edu-text h3 { font-size: 1.5rem; margin-bottom: 4px; }
        .edu-text span { color: var(--accent-purple); font-weight: 600; font-size: 0.9rem; }

        /* --- 9. FOOTER --- */
        footer {
            border-top: 1px solid var(--glass-border);
            padding: 60px 10%;
            background: #020202;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .socials { display: flex; gap: 20px; }

        .social-link {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.05);
            display: flex;
            align-items: center;
            justify-content: center;
            color: #fff;
            text-decoration: none;
            transition: 0.3s;
        }

        .social-link:hover {
            background: var(--accent-purple);
            transform: scale(1.1);
        }

        /* --- 10. SCROLL ANIMATION UTILS (The "Pop Up" Effect) --- */
        .hidden {
            opacity: 0;
            transform: translateY(40px); /* Start slightly lower */
            transition: all 0.8s cubic-bezier(0.16, 1, 0.3, 1); /* Smooth Apple-like easing */
        }

        .show {
            opacity: 1;
            transform: translateY(0);
        }
        
        /* Stagger delays for grid items */
        .delay-100 { transition-delay: 0.1s; }
        .delay-200 { transition-delay: 0.2s; }
        .delay-300 { transition-delay: 0.3s; }

        @media (max-width: 768px) {
            .hero { flex-direction: column-reverse; text-align: center; padding-top: 140px; }
            .nav-links { display: none; }
            .image-wrapper { width: 300px; height: 300px; margin: 0 auto; }
            h1 { font-size: 2.5rem; }
            .btn-group { justify-content: center; }
            footer { flex-direction: column; gap: 20px; text-align: center; }
        }
    </style>
</head>
<body>

    <div class="glow-blob"></div>
    <div class="glow-blob"></div>

    <nav>
        <div class="brand">SHUBHAM<span>VARMA</span></div>
        <div class="nav-links">
            <a href="#home">Home</a>
            <a href="#work">Work</a>
            <a href="#education">Education</a>
            <a href="#contact">Contact</a>
        </div>
    </nav>

    <section class="hero" id="home">
        <div class="hero-content hidden">
            <div class="pill">Founder @ Quicksite India</div>
            <h1>Building Intelligence <br><span>with AI & IoT</span></h1>
            <p class="subtitle">
                I am Shubham Sanjay Varma. I bridge the gap between hardware and software, creating intelligent systems that think and interact.
            </p>
            <div class="btn-group">
                <a href="#work" class="btn btn-primary">View Projects</a>
                <a href="#contact" class="btn btn-secondary">Contact Me</a>
            </div>
        </div>

        <div class="image-wrapper hidden delay-200">
            <img src="profile.jpg" alt="Shubham Varma" class="profile-img">
        </div>
    </section>

    <section id="education">
        <div class="section-header hidden">
            <h2 class="section-title">Education</h2>
            <p class="section-desc">My academic foundation in technology.</p>
        </div>
        
        <div class="edu-card hidden delay-100">
            <div class="card-icon" style="margin-bottom: 0;">
                <i class="fas fa-graduation-cap"></i>
            </div>
            <div class="edu-text">
                <h3>B.Tech Computer Science (AI & ML)</h3>
                <span>First Year • Current</span>
                <p style="color: #a1a1aa; font-size: 0.9rem; margin-top: 5px;">Specializing in Neural Networks, Deep Learning architectures, and Embedded Systems.</p>
            </div>
        </div>
    </section>

    <section id="work">
        <div class="section-header hidden">
            <h2 class="section-title">Featured Work</h2>
            <p class="section-desc">Selected projects in AI, Web Development, and IoT.</p>
        </div>

        <div class="grid-3">
            <div class="card hidden delay-100">
                <div class="card-icon"><i class="fas fa-id-card"></i></div>
                <h3>VeriDocs AI</h3>
                <p>An AI-powered document verification system designed to detect fraud in real-time using Computer Vision. Built for hackathons to automate ID checks.</p>
                <div class="tags">
                    <span class="tag">Python</span>
                    <span class="tag">OpenCV</span>
                    <span class="tag">AI/ML</span>
                </div>
            </div>

            <div class="card hidden delay-200">
                <div class="card-icon"><i class="fas fa-shopping-bag"></i></div>
                <h3>SV Digital Mart</h3>
                <p>A complete Full-Stack e-commerce solution. Features include secure payments, dynamic product inventory, and user authentication.</p>
                <div class="tags">
                    <span class="tag">Full Stack</span>
                    <span class="tag">Web Dev</span>
                    <span class="tag">Database</span>
                </div>
            </div>

            <div class="card hidden delay-300">
                <div class="card-icon"><i class="fas fa-trash-alt"></i></div>
                <h3>Smart Dustbin</h3>
                <p>IoT-based waste management system using Ultrasonic sensors and Servo motors to open automatically, improving hygiene and sanitation.</p>
                <div class="tags">
                    <span class="tag">Arduino</span>
                    <span class="tag">IoT</span>
                    <span class="tag">C++</span>
                </div>
            </div>
        </div>
    </section>

    <footer id="contact">
        <div>
            <div class="brand" style="margin-bottom: 10px;">SHUBHAM<span>VARMA</span></div>
            <p style="color: #666; font-size: 0.9rem;">&copy; 2026 Quicksite India. All rights reserved.</p>
            <p style="color: #666; font-size: 0.9rem; margin-top: 5px;">Thane, Mumbai, Maharashtra</p>
        </div>

        <div class="socials">
            <a href="mailto:varmashubhamsanjay@gmail.com" class="social-link" title="Email"><i class="fas fa-envelope"></i></a>
            <a href="https://github.com/varmashubhamsanjay" target="_blank" class="social-link" title="GitHub"><i class="fab fa-github"></i></a>
            <a href="https://www.linkedin.com/in/shubham-sanjay-varma-036090380?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" target="_blank" class="social-link" title="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
            <a href="https://www.instagram.com/shubhamvarmaaa?igsh=YmQ0cHg3bXNpNGNt" target="_blank" class="social-link" title="Instagram"><i class="fab fa-instagram"></i></a>
        </div>
    </footer>

    <script>
        // Professional Intersection Observer for Smooth Reveal
        const observerOptions = {
            root: null,
            rootMargin: '0px',
            threshold: 0.1 // Trigger when 10% of the element is visible
        };

        const observer = new IntersectionObserver((entries, observer) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('show');
                    // Optional: Unobserve if you only want it to animate once
                    // observer.unobserve(entry.target); 
                } else {
                    // Optional: Remove class to re-animate when scrolling UP (The "Pop Up" Effect)
                    // If you find this annoying/dizzying, comment out the line below.
                    entry.target.classList.remove('show'); 
                }
            });
        }, observerOptions);

        const hiddenElements = document.querySelectorAll('.hidden');
        hiddenElements.forEach((el) => observer.observe(el));
    </script>
</body>
</html>
