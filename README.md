<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Husnain - Full Stack Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Section */
        .header {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(20px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.2);
            padding: 2rem 0;
            text-align: center;
            margin-bottom: 2rem;
        }

        .header h1 {
            font-size: 3.5rem;
            color: #fff;
            margin-bottom: 0.5rem;
            text-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            animation: fadeInUp 1s ease-out;
        }

        .header .subtitle {
            font-size: 1.3rem;
            color: rgba(255, 255, 255, 0.9);
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease-out 0.2s both;
        }

        .header .description {
            max-width: 800px;
            margin: 0 auto;
            color: rgba(255, 255, 255, 0.8);
            font-size: 1.1rem;
            animation: fadeInUp 1s ease-out 0.4s both;
        }

        /* Card Styles */
        .card {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(20px);
            border-radius: 20px;
            padding: 2rem;
            margin-bottom: 2rem;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.3);
            transition: all 0.3s ease;
            animation: slideInUp 0.8s ease-out;
        }

        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 25px 45px rgba(0, 0, 0, 0.15);
        }

        .card h2 {
            color: #4a5568;
            font-size: 2rem;
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .emoji {
            font-size: 1.5rem;
        }

        /* Tech Stack Grid */
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-top: 1rem;
        }

        .tech-category {
            background: linear-gradient(135deg, #f7fafc 0%, #edf2f7 100%);
            border-radius: 15px;
            padding: 1.5rem;
            transition: all 0.3s ease;
        }

        .tech-category:hover {
            transform: scale(1.02);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        .tech-category h3 {
            color: #2d3748;
            margin-bottom: 1rem;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .tech-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .tech-tag {
            background: linear-gradient(135deg, #4299e1 0%, #3182ce 100%);
            color: white;
            padding: 0.4rem 1rem;
            border-radius: 25px;
            font-size: 0.9rem;
            font-weight: 500;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .tech-tag:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(66, 153, 225, 0.4);
        }

        /* Services Grid */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
            margin-top: 1rem;
        }

        .service-item {
            background: linear-gradient(135deg, #f0fff4 0%, #e6fffa 100%);
            border-radius: 15px;
            padding: 1.5rem;
            text-align: center;
            transition: all 0.3s ease;
            border-left: 4px solid #48bb78;
        }

        .service-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 25px rgba(72, 187, 120, 0.2);
        }

        .service-item .service-icon {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .service-item h3 {
            color: #2d3748;
            margin-bottom: 0.5rem;
        }

        .service-item p {
            color: #4a5568;
            font-size: 0.95rem;
        }

        /* Focus Items */
        .focus-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1rem;
            margin-top: 1rem;
        }

        .focus-item {
            background: linear-gradient(135deg, #fef5e7 0%, #fed7aa 100%);
            border-radius: 12px;
            padding: 1.2rem;
            display: flex;
            align-items: center;
            gap: 1rem;
            transition: all 0.3s ease;
        }

        .focus-item:hover {
            transform: scale(1.02);
            box-shadow: 0 8px 16px rgba(251, 191, 36, 0.2);
        }

        .focus-item .focus-icon {
            font-size: 1.8rem;
        }

        .focus-item .focus-text {
            color: #744210;
            font-weight: 500;
        }

        /* Contact Section */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-top: 1rem;
        }

        .contact-item {
            background: linear-gradient(135deg, #e6fffa 0%, #b2f5ea 100%);
            border-radius: 15px;
            padding: 1.5rem;
            text-align: center;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .contact-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 25px rgba(56, 178, 172, 0.2);
        }

        .contact-item .contact-icon {
            font-size: 2rem;
            margin-bottom: 1rem;
            color: #319795;
        }

        .contact-item h3 {
            color: #2d3748;
            margin-bottom: 0.5rem;
        }

        .contact-item p {
            color: #4a5568;
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
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

        /* Floating Animation for Background Elements */
        .floating-shapes {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .shape {
            position: absolute;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }

        .shape:nth-child(1) {
            width: 80px;
            height: 80px;
            top: 20%;
            left: 10%;
            animation-delay: 0s;
        }

        .shape:nth-child(2) {
            width: 120px;
            height: 120px;
            top: 60%;
            right: 10%;
            animation-delay: 2s;
        }

        .shape:nth-child(3) {
            width: 60px;
            height: 60px;
            top: 80%;
            left: 20%;
            animation-delay: 4s;
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0px) rotate(0deg);
            }
            50% {
                transform: translateY(-20px) rotate(180deg);
            }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2.5rem;
            }
            
            .header .subtitle {
                font-size: 1.1rem;
            }
            
            .tech-grid {
                grid-template-columns: 1fr;
            }
            
            .card {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="floating-shapes">
        <div class="shape"></div>
        <div class="shape"></div>
        <div class="shape"></div>
    </div>

    <div class="header">
        <div class="container">
            <h1>👋 Hey there! I'm Husnain</h1>
            <p class="subtitle">Full Stack Developer (MERN) from Pakistan</p>
            <p class="description">
                Building scalable, secure, and user-centric applications with a strong focus on solving complex problems, 
                designing efficient backend systems, and crafting engaging frontend experiences that bring ideas to life.
            </p>
        </div>
    </div>

    <div class="container">
        <!-- Tech Stack Section -->
        <div class="card">
            <h2><span class="emoji">🔧</span> Tech Stack</h2>
            <div class="tech-grid">
                <div class="tech-category">
                    <h3><span class="emoji">💻</span> Languages</h3>
                    <div class="tech-tags">
                        <span class="tech-tag">JavaScript</span>
                        <span class="tech-tag">TypeScript</span>
                        <span class="tech-tag">Java</span>
                        <span class="tech-tag">C++</span>
                        <span class="tech-tag">C#</span>
                        <span class="tech-tag">HTML</span>
                        <span class="tech-tag">CSS</span>
                        <span class="tech-tag">SCSS</span>
                        <span class="tech-tag">SQL</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3><span class="emoji">🧰</span> Frameworks & Libraries</h3>
                    <div class="tech-tags">
                        <span class="tech-tag">React.js</span>
                        <span class="tech-tag">React Native</span>
                        <span class="tech-tag">Next.js</span>
                        <span class="tech-tag">Tailwind CSS</span>
                        <span class="tech-tag">Framer Motion</span>
                        <span class="tech-tag">Node.js</span>
                        <span class="tech-tag">Express.js</span>
                        <span class="tech-tag">RESTful APIs</span>
                        <span class="tech-tag">GraphQL</span>
                        <span class="tech-tag">Supabase</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3><span class="emoji">🗄️</span> Databases</h3>
                    <div class="tech-tags">
                        <span class="tech-tag">MongoDB</span>
                        <span class="tech-tag">PostgreSQL</span>
                        <span class="tech-tag">Redis</span>
                        <span class="tech-tag">MySQL</span>
                        <span class="tech-tag">Firebase</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3><span class="emoji">📦</span> Messaging & Queues</h3>
                    <div class="tech-tags">
                        <span class="tech-tag">Apache Kafka</span>
                        <span class="tech-tag">RabbitMQ</span>
                        <span class="tech-tag">BullMQ</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3><span class="emoji">🛠️</span> Tools & Platforms</h3>
                    <div class="tech-tags">
                        <span class="tech-tag">Git</span>
                        <span class="tech-tag">GitHub</span>
                        <span class="tech-tag">Vite</span>
                        <span class="tech-tag">Docker</span>
                        <span class="tech-tag">Docker Compose</span>
                        <span class="tech-tag">NGINX</span>
                        <span class="tech-tag">cPanel</span>
                        <span class="tech-tag">Postman</span>
                        <span class="tech-tag">Mocha</span>
                        <span class="tech-tag">Ubuntu Server</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3><span class="emoji">⚙️</span> Architecture</h3>
                    <div class="tech-tags">
                        <span class="tech-tag">Microservices</span>
                        <span class="tech-tag">Database Design</span>
                        <span class="tech-tag">System Design</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- What I Do Section -->
        <div class="card">
            <h2><span class="emoji">🚀</span> What I Do</h2>
            <p style="margin-bottom: 2rem; color: #4a5568; font-size: 1.1rem;">
                I specialize in turning ideas into robust, production-ready solutions—whether it's:
            </p>
            <div class="services-grid">
                <div class="service-item">
                    <div class="service-icon">🖥️</div>
                    <h3>Dynamic Web Apps</h3>
                    <p>Smooth UIs and real-time interactions that engage users</p>
                </div>
                <div class="service-item">
                    <div class="service-icon">🔐</div>
                    <h3>Secure Backend Systems</h3>
                    <p>Designed for scale and performance with robust architecture</p>
                </div>
                <div class="service-item">
                    <div class="service-icon">📡</div>
                    <h3>Real-time Communication</h3>
                    <p>Platforms powered by sockets and message queues</p>
                </div>
                <div class="service-item">
                    <div class="service-icon">🤖</div>
                    <h3>AI-Integrated Applications</h3>
                    <p>Computer vision and automation solutions</p>
                </div>
                <div class="service-item">
                    <div class="service-icon">☁️</div>
                    <h3>Cloud-Deployed Services</h3>
                    <p>Using Docker and CI/CD workflows for seamless deployment</p>
                </div>
            </div>
            <p style="margin-top: 2rem; color: #4a5568; font-size: 1.1rem; text-align: center; font-style: italic;">
                At the core, I enjoy building end-to-end solutions that are not only functional but also impactful, adaptable, and future-ready.
            </p>
        </div>

        <!-- Current Focus Section -->
        <div class="card">
            <h2><span class="emoji">📈</span> Current Focus</h2>
            <div class="focus-grid">
                <div class="focus-item">
                    <div class="focus-icon">🧱</div>
                    <div class="focus-text">Architecting scalable backend systems using microservices & queues</div>
                </div>
                <div class="focus-item">
                    <div class="focus-icon">🎨</div>
                    <div class="focus-text">Elevating UI/UX with responsive layouts and fluid animations</div>
                </div>
                <div class="focus-item">
                    <div class="focus-icon">🔐</div>
                    <div class="focus-text">Implementing strong security practices in modern auth flows</div>
                </div>
                <div class="focus-item">
                    <div class="focus-icon">🐳</div>
                    <div class="focus-text">Expanding expertise in Docker, DevOps, and cloud-native environments</div>
                </div>
            </div>
        </div>

        <!-- Contact Section -->
        <div class="card">
            <h2><span class="emoji">📬</span> Let's Connect</h2>
            <p style="margin-bottom: 2rem; color: #4a5568; font-size: 1.1rem; text-align: center;">
                Always open to collaborating on challenging projects, innovative ideas, or impactful solutions.
            </p>
            <div class="contact-grid">
                <div class="contact-item" onclick="window.open('https://github.com/husnainiqbal', '_blank')">
                    <div class="contact-icon">🌐</div>
                    <h3>Portfolio</h3>
                    <p>Coming Soon</p>
                </div>
                <div class="contact-item" onclick="window.location.href='mailto:husnainiqbal577@gmail.com'">
                    <div class="contact-icon">📧</div>
                    <h3>Email</h3>
                    <p>husnainiqbal577@gmail.com</p>
                </div>
                <div class="contact-item" onclick="window.open('https://wa.me/923424136198', '_blank')">
                    <div class="contact-icon">📱</div>
                    <h3>WhatsApp</h3>
                    <p>+92 342 413 6198</p>
                </div>
            </div>
            <div style="text-align: center; margin-top: 2rem;">
                <p style="font-size: 1.2rem; color: #4a5568; font-weight: 500;">
                    ✨ Let's create something extraordinary together!
                </p>
            </div>
        </div>
    </div>

    <script>
        // Add some interactive animations
        document.addEventListener('DOMContentLoaded', function() {
            const cards = document.querySelectorAll('.card');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach((entry) => {
                    if (entry.isIntersecting) {
                        entry.target.style.animation = 'slideInUp 0.8s ease-out';
                    }
                });
            });

            cards.forEach((card) => {
                observer.observe(card);
            });

            // Add click animation to tech tags
            const techTags = document.querySelectorAll('.tech-tag');
            techTags.forEach(tag => {
                tag.addEventListener('click', function() {
                    this.style.transform = 'scale(0.95)';
                    setTimeout(() => {
                        this.style.transform = 'translateY(-2px)';
                    }, 150);
                });
            });
        });
    </script>
</body>
</html>
