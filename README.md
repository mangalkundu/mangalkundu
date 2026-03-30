<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Mangal Kundu · Data Analyst Portfolio</title>
    <!-- Google Fonts & Font Awesome -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- Animate.css (lightweight) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"/>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(145deg, #f9faff 0%, #edf2fc 100%);
            color: #1a2c3e;
            line-height: 1.45;
            scroll-behavior: smooth;
        }

        /* custom animated gradient border & glassmorphism */
        .glass-card {
            background: rgba(255, 255, 255, 0.75);
            backdrop-filter: blur(10px);
            border-radius: 2rem;
            box-shadow: 0 20px 35px -12px rgba(0, 0, 0, 0.1), 0 0 0 1px rgba(255,255,255,0.6);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .glass-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 28px 40px -18px rgba(0, 0, 0, 0.2);
        }

        .animated-bg {
            background: radial-gradient(circle at 10% 20%, rgba(68, 126, 255, 0.08), rgba(0, 212, 255, 0.02));
        }

        .btn-glow {
            transition: all 0.2s ease;
            box-shadow: 0 2px 6px rgba(0, 0, 0, 0.05);
        }
        .btn-glow:hover {
            transform: scale(1.02);
            box-shadow: 0 8px 20px rgba(0, 100, 200, 0.2);
        }

        /* typing animation */
        .typing-demo {
            display: inline-block;
            overflow: hidden;
            border-right: 0.15em solid #2c7da0;
            white-space: nowrap;
            letter-spacing: 0.02em;
            animation: typing 2.2s steps(30, end), blink-caret 0.7s step-end infinite;
        }
        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }
        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: #2c7da0; }
        }

        /* floating icons animation */
        @keyframes float {
            0% { transform: translateY(0px) rotate(0deg); }
            100% { transform: translateY(-8px) rotate(3deg); }
        }
        .float-icon {
            animation: float 3s infinite alternate ease-in-out;
        }

        .skill-badge {
            transition: all 0.2s cubic-bezier(0.2, 0.9, 0.4, 1.1);
        }
        .skill-badge:hover {
            transform: translateY(-3px) scale(1.03);
            filter: brightness(1.02);
        }

        /* project cards animations on scroll (reveal) */
        .project-card {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.6s ease, transform 0.5s ease;
        }
        .project-card.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .gradient-text {
            background: linear-gradient(120deg, #1F3B4C, #2A6F8F, #1F7A8C);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            background-size: 200% auto;
            animation: shimmer 5s linear infinite;
        }
        @keyframes shimmer {
            0% { background-position: 0% center; }
            100% { background-position: 200% center; }
        }

        .social-icon {
            transition: all 0.25s ease;
            display: inline-flex;
            align-items: center;
            justify-content: center;
        }
        .social-icon:hover {
            transform: translateY(-5px) scale(1.08);
            filter: drop-shadow(0 6px 12px rgba(0,0,0,0.15));
        }

        @media (max-width: 680px) {
            .container {
                padding-left: 1.2rem;
                padding-right: 1.2rem;
            }
            .typing-demo {
                white-space: normal;
                border-right: none;
                animation: none;
                display: inline;
            }
        }
    </style>
</head>
<body class="animated-bg">

    <div class="container max-w-5xl mx-auto px-5 py-8 md:py-12">
        <!-- Header Section with animated avatar and greeting -->
        <div class="glass-card p-6 md:p-10 mb-10 animate__animated animate__fadeInUp">
            <div class="flex flex-col md:flex-row items-center gap-8">
                <div class="relative">
                    <div class="w-32 h-32 md:w-40 md:h-40 rounded-full bg-gradient-to-tr from-[#2c7da0] to-[#61a5c2] flex items-center justify-center shadow-xl float-icon">
                        <span class="text-5xl md:text-6xl font-bold text-white">MK</span>
                    </div>
                    <div class="absolute -bottom-2 -right-2 bg-white rounded-full p-2 shadow-md">
                        <i class="fas fa-chart-line text-[#2c7da0] text-xl"></i>
                    </div>
                </div>
                <div class="text-center md:text-left">
                    <h1 class="text-4xl md:text-5xl font-extrabold tracking-tight">
                        <span class="gradient-text">Mangal Kundu</span>
                    </h1>
                    <div class="flex flex-wrap justify-center md:justify-start gap-2 mt-3">
                        <span class="inline-flex items-center gap-1 bg-white/60 rounded-full px-4 py-1.5 text-sm font-medium backdrop-blur-sm shadow-sm">
                            <i class="fas fa-graduation-cap text-[#2c7da0]"></i> BTech CS Graduate
                        </span>
                        <span class="inline-flex items-center gap-1 bg-white/60 rounded-full px-4 py-1.5 text-sm font-medium">
                            <i class="fas fa-chart-simple text-[#2c7da0]"></i> Data Analyst
                        </span>
                        <span class="inline-flex items-center gap-1 bg-white/60 rounded-full px-4 py-1.5 text-sm font-medium">
                            <i class="fas fa-code"></i> Dev Enthusiast
                        </span>
                    </div>
                    <div class="mt-4 text-lg md:text-xl text-gray-700 max-w-2xl">
                        <span class="typing-demo font-semibold">📊 Passionate about Data Analysis · SQL · Python</span>
                        <p class="mt-3 text-gray-600">Turning raw data into actionable insights. Strong foundation in databases, analytical thinking, and modern data workflows.</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- Skills Section with animated icons & hover effects -->
        <div class="glass-card p-6 md:p-8 mb-10 animate__animated animate__fadeInUp animate__delay-0.2s">
            <div class="flex items-center gap-3 mb-6 border-b border-gray-200/70 pb-3">
                <i class="fas fa-cogs text-3xl text-[#2c7da0]"></i>
                <h2 class="text-2xl md:text-3xl font-bold tracking-tight">Tech Arsenal</h2>
                <span class="bg-black/5 px-3 py-1 rounded-full text-xs font-mono">⚡ interactive</span>
            </div>
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-5">
                <!-- Database -->
                <div class="bg-white/50 rounded-2xl p-4 backdrop-blur-sm shadow-sm skill-badge transition-all hover:shadow-md">
                    <div class="flex items-center gap-3 mb-2">
                        <i class="fas fa-database text-3xl text-blue-600"></i>
                        <span class="font-bold text-lg">Database</span>
                    </div>
                    <div class="flex flex-wrap gap-2 mt-2">
                        <span class="bg-blue-100 text-blue-800 px-3 py-1 rounded-full text-sm flex items-center gap-1"><i class="fab fa-sql"></i> SQL</span>
                        <span class="bg-blue-100 text-blue-800 px-3 py-1 rounded-full text-sm"><i class="fas fa-database"></i> MySQL</span>
                        <span class="bg-blue-100 text-blue-800 px-3 py-1 rounded-full text-sm">DBMS</span>
                        <span class="bg-blue-100 text-blue-800 px-3 py-1 rounded-full text-sm">Query Tuning</span>
                    </div>
                </div>
                <!-- Programming -->
                <div class="bg-white/50 rounded-2xl p-4 backdrop-blur-sm shadow-sm skill-badge">
                    <div class="flex items-center gap-3 mb-2">
                        <i class="fab fa-python text-3xl text-[#3776AB]"></i>
                        <span class="font-bold text-lg">Programming</span>
                    </div>
                    <div class="flex flex-wrap gap-2 mt-2">
                        <span class="bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">Python</span>
                        <span class="bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">Pandas</span>
                        <span class="bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">OOP</span>
                    </div>
                </div>
                <!-- Visualization -->
                <div class="bg-white/50 rounded-2xl p-4 backdrop-blur-sm shadow-sm skill-badge">
                    <div class="flex items-center gap-3 mb-2">
                        <i class="fas fa-chart-pie text-3xl text-[#E97627]"></i>
                        <span class="font-bold text-lg">Visualization</span>
                    </div>
                    <div class="flex flex-wrap gap-2 mt-2">
                        <span class="bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-sm">Tableau</span>
                        <span class="bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-sm">Matplotlib</span>
                        <span class="bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-sm">Dashboards</span>
                    </div>
                </div>
                <!-- Analytical -->
                <div class="bg-white/50 rounded-2xl p-4 backdrop-blur-sm shadow-sm skill-badge">
                    <div class="flex items-center gap-3 mb-2">
                        <i class="fas fa-brain text-3xl text-purple-600"></i>
                        <span class="font-bold text-lg">Mindset</span>
                    </div>
                    <div class="flex flex-wrap gap-2 mt-2">
                        <span class="bg-purple-100 text-purple-800 px-3 py-1 rounded-full text-sm">Problem Solving</span>
                        <span class="bg-purple-100 text-purple-800 px-3 py-1 rounded-full text-sm">Analytical Thinking</span>
                        <span class="bg-purple-100 text-purple-800 px-3 py-1 rounded-full text-sm">Storytelling</span>
                    </div>
                </div>
            </div>
            <!-- additional detail row -->
            <div class="mt-6 flex flex-wrap justify-center gap-4 text-sm text-gray-600 border-t border-gray-200 pt-5">
                <div class="flex gap-1 items-center"><i class="fas fa-check-circle text-green-500"></i> <span>Advanced SQL (Joins, Aggregations, Subqueries)</span></div>
                <div class="flex gap-1 items-center"><i class="fas fa-check-circle text-green-500"></i> <span>Data Cleaning & Wrangling</span></div>
                <div class="flex gap-1 items-center"><i class="fas fa-chart-line text-blue-500"></i> <span>Interactive Dashboards</span></div>
            </div>
        </div>

        <!-- Featured Projects Section with reveal animation -->
        <div class="mb-10">
            <div class="flex items-center gap-2 mb-6">
                <i class="fas fa-code-branch text-3xl text-[#2c7da0] animate-pulse"></i>
                <h2 class="text-2xl md:text-3xl font-bold tracking-tight">✨ Featured Work</h2>
                <div class="h-1 w-16 bg-gradient-to-r from-[#2c7da0] to-[#a9d6e5] rounded-full"></div>
            </div>
            <div class="grid md:grid-cols-2 gap-7">
                <!-- SQL Portfolio Card -->
                <div class="project-card glass-card p-6 transition-all duration-300 hover:shadow-2xl" id="card1">
                    <div class="flex items-center justify-between mb-3">
                        <i class="fas fa-database text-4xl text-blue-600"></i>
                        <span class="bg-gray-200/70 px-3 py-1 rounded-full text-xs font-mono">SQL · Analytics</span>
                    </div>
                    <h3 class="text-2xl font-bold mb-2">📁 SQL Portfolio</h3>
                    <p class="text-gray-600 mb-4">Collection of advanced SQL queries — joins, aggregations, subqueries, window functions, and database design patterns. Perfect showcase of data extraction expertise.</p>
                    <div class="flex flex-wrap gap-3 mt-2">
                        <a href="https://github.com/mangalkundu/sql-portfolio" target="_blank" class="inline-flex items-center gap-2 bg-gray-900 text-white px-5 py-2.5 rounded-xl text-sm font-semibold btn-glow hover:bg-gray-800 transition"><i class="fab fa-github"></i> View Repository</a>
                        <span class="inline-flex items-center gap-1 text-sm text-gray-500"><i class="fas fa-star text-yellow-500"></i> 15+ query examples</span>
                    </div>
                </div>
                <!-- FutureNFT Marketplace -->
                <div class="project-card glass-card p-6 transition-all duration-300 hover:shadow-2xl" id="card2">
                    <div class="flex items-center justify-between mb-3">
                        <i class="fas fa-globe text-4xl text-indigo-500"></i>
                        <span class="bg-gray-200/70 px-3 py-1 rounded-full text-xs font-mono">Web3 · Live</span>
                    </div>
                    <h3 class="text-2xl font-bold mb-2">🌐 FutureNFT Marketplace</h3>
                    <p class="text-gray-600 mb-4">Live NFT marketplace website — real-world deployment, database integration, frontend management. Gained hands-on experience in deployment pipelines and user data flows.</p>
                    <div class="flex flex-wrap gap-3 mt-2">
                        <a href="https://github.com/mangalkundu/futurenft-marketplace" target="_blank" class="inline-flex items-center gap-2 bg-gray-800 text-white px-5 py-2.5 rounded-xl text-sm font-semibold btn-glow"><i class="fab fa-github"></i> GitHub Repo</a>
                        <a href="https://futurenft.io/" target="_blank" class="inline-flex items-center gap-2 bg-gradient-to-r from-blue-500 to-cyan-500 text-white px-5 py-2.5 rounded-xl text-sm font-semibold btn-glow shadow-md"><i class="fas fa-external-link-alt"></i> Live Demo</a>
                    </div>
                </div>
            </div>
            <!-- extra micro project note -->
            <div class="mt-6 text-center text-sm text-gray-500 italic">
                <i class="fas fa-chart-line"></i> more data case studies & dashboards available upon request — open for collaboration
            </div>
        </div>

        <!-- Stats / fun animated counter section (adds vibe) -->
        <div class="glass-card p-6 mb-10 bg-white/60 backdrop-blur-sm">
            <div class="grid grid-cols-2 md:grid-cols-4 gap-5 text-center">
                <div class="flex flex-col items-center">
                    <i class="fas fa-code text-3xl text-indigo-500 mb-2"></i>
                    <div class="text-2xl font-black counter" data-target="8">0+</div>
                    <span class="text-sm uppercase tracking-wide text-gray-600">Projects</span>
                </div>
                <div class="flex flex-col items-center">
                    <i class="fas fa-database text-3xl text-blue-500 mb-2"></i>
                    <div class="text-2xl font-black counter" data-target="50">0+</div>
                    <span class="text-sm uppercase tracking-wide text-gray-600">SQL challenges</span>
                </div>
                <div class="flex flex-col items-center">
                    <i class="fas fa-chart-line text-3xl text-green-500 mb-2"></i>
                    <div class="text-2xl font-black counter" data-target="12">0+</div>
                    <span class="text-sm uppercase tracking-wide text-gray-600">Dashboards</span>
                </div>
                <div class="flex flex-col items-center">
                    <i class="fas fa-users text-3xl text-amber-500 mb-2"></i>
                    <div class="text-2xl font-black counter" data-target="100">0+</div>
                    <span class="text-sm uppercase tracking-wide text-gray-600">Coffee chats ☕</span>
                </div>
            </div>
        </div>

        <!-- Connect Section + animated socials -->
        <div class="glass-card p-7 md:p-9 text-center animate__animated animate__fadeInUp animate__delay-0.3s">
            <div class="mb-4 relative inline-block">
                <i class="fas fa-paper-plane text-5xl text-[#2c7da0] float-icon"></i>
            </div>
            <h3 class="text-2xl font-bold mb-2">Let’s connect & build data stories</h3>
            <p class="text-gray-600 max-w-xl mx-auto mb-6">Open to Data Analyst roles · Available immediately — love solving problems with SQL, Python, and visualization tools.</p>
            <div class="flex flex-wrap justify-center gap-5 mb-6">
                <a href="https://www.linkedin.com/in/mangalkundu" target="_blank" class="social-icon bg-[#0077B5] text-white rounded-full p-3 w-14 h-14 flex items-center justify-center text-2xl shadow-lg transition-all"><i class="fab fa-linkedin-in"></i></a>
                <a href="mailto:kundumangal876@gmail.com" class="social-icon bg-gradient-to-br from-red-500 to-red-600 text-white rounded-full p-3 w-14 h-14 flex items-center justify-center text-2xl shadow-lg"><i class="fas fa-envelope"></i></a>
                <a href="https://github.com/mangalkundu" target="_blank" class="social-icon bg-gray-800 text-white rounded-full p-3 w-14 h-14 flex items-center justify-center text-2xl shadow-lg"><i class="fab fa-github"></i></a>
                <a href="#" class="social-icon bg-[#1DA1F2] text-white rounded-full p-3 w-14 h-14 flex items-center justify-center text-2xl shadow-lg opacity-80 hover:opacity-100"><i class="fab fa-twitter"></i></a>
            </div>
            <div class="border-t border-gray-200/70 pt-5 mt-2 text-sm text-gray-500 flex flex-wrap justify-center gap-5">
                <span><i class="fas fa-map-marker-alt mr-1"></i> India · Remote Ready</span>
                <span><i class="fas fa-briefcase"></i> Immediate Joiner</span>
                <span><i class="fas fa-certificate"></i> BTech CSE Graduate</span>
            </div>
            <div class="mt-5 text-xs text-gray-400">
                ⭐️ Portfolio crafted with data-driven passion — let’s turn insights into impact.
            </div>
        </div>
    </div>

    <!-- Scroll reveal & counter animation script -->
    <script>
        // Intersection Observer for project cards fade-in + counters
        const projectCards = document.querySelectorAll('.project-card');
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                    observer.unobserve(entry.target);
                }
            });
        }, { threshold: 0.2 });

        projectCards.forEach(card => {
            observer.observe(card);
        });

        // manually set visible if already visible on load? fallback: add visible class for cards that are already visible
        // also run counter when counters container becomes visible
        const counters = document.querySelectorAll('.counter');
        const counterSection = document.querySelector('.glass-card .grid');
        let counted = false;

        function startCounters() {
            if (counted) return;
            counted = true;
            counters.forEach(counter => {
                const target = parseInt(counter.getAttribute('data-target'));
                let current = 0;
                const increment = target / 40; // smooth
                const updateCounter = () => {
                    current += increment;
                    if (current < target) {
                        counter.innerText = Math.ceil(current) + (target > 50 ? '+' : '');
                        requestAnimationFrame(updateCounter);
                    } else {
                        counter.innerText = target + (target > 50 ? '+' : '');
                    }
                };
                updateCounter();
            });
        }

        const counterObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting && !counted) {
                    startCounters();
                }
            });
        }, { threshold: 0.4 });
        if (counterSection) counterObserver.observe(counterSection);

        // also for cards to set visible class if they are already visible (like first load)
        window.addEventListener('load', () => {
            projectCards.forEach(card => {
                const rect = card.getBoundingClientRect();
                if (rect.top < window.innerHeight - 100) {
                    card.classList.add('visible');
                }
            });
            // preload any counters if already visible (scroll position)
            if (counterSection) {
                const rect = counterSection.getBoundingClientRect();
                if (rect.top < window.innerHeight - 80) startCounters();
            }
        });

        // additional floating hover micro-interactions for skill badges
        const badges = document.querySelectorAll('.skill-badge');
        badges.forEach(badge => {
            badge.addEventListener('mouseenter', (e) => {
                badge.style.transition = 'all 0.2s ease';
            });
        });
    </script>
</body>
</html>
