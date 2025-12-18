<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NOIR ÉLAN CAFÉ</title>
    <style>
        /* Reset and Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Times New Roman', serif;
            background-color: #000000; /* Deep black */
            color: #f8f8f2; /* Warm white */
            line-height: 1.6;
            overflow-x: hidden;
            scroll-behavior: smooth;
        }
        h1, h2, h3 {
            font-family: 'Helvetica Neue', Arial, sans-serif;
            font-weight: 300;
        }
        h1 {
            font-size: 3rem;
            letter-spacing: 0.05em;
            color: #8b4513; /* Espresso brown */
        }
        h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: #8b4513;
        }
        h3 {
            font-size: 1.8rem;
            margin-bottom: 0.5rem;
        }
        p {
            font-size: 1.1rem;
            margin-bottom: 1rem;
        }
        blockquote {
            font-style: italic;
            font-size: 1.3rem;
            border-left: 3px solid #8b4513;
            padding-left: 1rem;
            margin: 2rem 0;
            color: #f8f8f2;
        }
        section {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 2rem;
            position: relative;
        }
        .card {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(139, 69, 19, 0.3);
            border-radius: 10px;
            padding: 1.5rem;
            margin: 1rem;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            max-width: 300px;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(139, 69, 19, 0.2);
        }
        .divider {
            width: 0;
            height: 2px;
            background: #8b4513;
            margin: 2rem 0;
            animation: dividerGrow 2s ease-out forwards;
        }
        @keyframes dividerGrow {
            to { width: 100%; }
        }
        .btn {
            background: #8b4513;
            color: #f8f8f2;
            padding: 1rem 2rem;
            border: none;
            border-radius: 5px;
            font-size: 1.2rem;
            cursor: pointer;
            transition: box-shadow 0.5s ease;
            margin-top: 1rem;
        }
        .btn:hover {
            box-shadow: 0 0 20px rgba(139, 69, 19, 0.5);
        }
        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }
        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
        .slide-in {
            opacity: 0;
            transform: translateX(-20px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }
        .slide-in.visible {
            opacity: 1;
            transform: translateX(0);
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1rem;
            width: 100%;
            max-width: 1000px;
        }
        .icon {
            width: 50px;
            height: 50px;
            fill: #8b4513;
            margin-bottom: 1rem;
        }
        /* Hero Specific */
        #hero {
            text-align: center;
            animation: heroLoad 1s ease-out;
        }
        @keyframes heroLoad {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }
        #hero .tagline {
            font-size: 1.2rem;
            margin-bottom: 1rem;
        }
        /* Contact Section */
        #contact {
            flex-direction: row;
            justify-content: space-around;
            align-items: flex-start;
            flex-wrap: wrap;
        }
        .contact-details {
            max-width: 400px;
            margin: 1rem;
        }
        .contact-form {
            max-width: 400px;
            margin: 1rem;
        }
        .form-group {
            position: relative;
            margin-bottom: 1.5rem;
        }
        .form-group input, .form-group textarea {
            width: 100%;
            padding: 1rem;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(139, 69, 19, 0.3);
            border-radius: 5px;
            color: #f8f8f2;
            font-size: 1rem;
            transition: border-color 0.3s ease;
        }
        .form-group input:focus, .form-group textarea:focus {
            border-color: #8b4513;
            outline: none;
        }
        .form-group label {
            position: absolute;
            top: 1rem;
            left: 1rem;
            color: #f8f8f2;
            pointer-events: none;
            transition: all 0.3s ease;
        }
        .form-group input:focus + label, .form-group textarea:focus + label,
        .form-group input:not(:placeholder-shown) + label, .form-group textarea:not(:placeholder-shown) + label {
            top: -0.5rem;
            left: 0.5rem;
            font-size: 0.8rem;
            color: #8b4513;
        }
        .form-group textarea {
            resize: vertical;
            min-height: 100px;
        }
        .submit-btn {
            width: 100%;
        }
        .message {
            margin-top: 1rem;
            font-size: 1rem;
        }
        .success { color: #8b4513; }
        .error { color: #ff6b6b; }
        /* Footer */
        footer {
            text-align: center;
            padding: 2rem;
            animation: footerFade 1s ease-out;
        }
        @keyframes footerFade {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        /* Responsive */
        @media (max-width: 768px) {
            h1 { font-size: 2rem; }
            h2 { font-size: 2rem; }
            .grid { grid-template-columns: 1fr; }
            #contact { flex-direction: column; }
        }
    </style>
</head>
<body>
    <section id="hero">
        <h1>NOIR ÉLAN CAFÉ</h1>
        <p class="tagline">Crafted in Detail. Served with Intention.</p>
        <h2>Where Coffee Becomes an Experience.</h2>
        <button class="btn">Explore Our World</button>
    </section>

    <section id="brand-story">
        <div class="fade-in">
            <h2>Brand Story</h2>
            <p>NOIR ÉLAN CAFÉ embodies the art of refined hospitality. We focus on creating spaces where every element serves a purpose, blending tradition with modern elegance.</p>
            <blockquote>True quality reveals itself in the quiet details.</blockquote>
        </div>
    </section>

    <section id="signature-experience">
        <h2>Signature Experience</h2>
        <div class="grid">
            <div class="card slide-in">
                <svg class="icon" viewBox="0 0 24 24">
                    <path d="M12 2c-1.1 0-2 .9-2 2v1H8c-.55 0-1 .45-1 1s.45 1 1 1h1v1c0 2.76 2.24 5 5 5s5-2.24 5-5V7h1c.55 0 1-.45 1-1s-.45-1-1-1h-2V4c0-1.1-.9-2-2-2zm0 2c.55 0 1 .45 1 1v1h-2V5c0-.55.45-1 1-1z"/>
                </svg>
                <h3>Craft</h3>
                <p>Each brew is crafted with meticulous care, highlighting the finest beans and expert roasting techniques.</p>
            </div>
            <div class="card slide-in">
                <svg class="icon" viewBox="0 0 24 24">
                    <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>
                </svg>
                <h3>Atmosphere</h3>
                <p>Our spaces are designed for calm reflection, where soft lighting and subtle sounds enhance the sensory experience.</p>
            </div>
            <div class="card slide-in">
                <svg class="icon" viewBox="0 0 24 24">
                    <path d="M9 11H7v2h2v-2zm4 0h-2v2h2v-2zm4 0h-2v2h2v-2zm2-7h-1V2h-2v2H8V2H6v2H5c-1.1 0-1.99.9-1.99 2L3 20c0 1.1.89 2 2 2h14c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 16H5V9h14v11z"/>
                </svg>
                <h3>Precision</h3>
                <p>From grind to pour, every step is executed with precision, ensuring consistency and excellence in every cup.</p>
            </div>
        </div>
    </section>

    <section id="philosophy">
        <div class="fade-in">
            <h2>Philosophy</h2>
            <p>We build trust through refined service and attention to detail. NOIR ÉLAN CAFÉ is for those who seek more than just a drink.</p>
            <p class="highlight">Designed for those who notice the difference.</p>
        </div>
    </section>

    <section id="contact">
        <div class="contact-details slide-in">
            <h2>Contact Us</h2>
            <p><strong>Address:</strong> 123 Noir Lane, Elegance City, EC 12345</p>
            <p><strong>Phone:</strong> (555) 123-4567</p>
            <p><strong>Email:</strong> hello@noirelancafe.com</p>
            <p><strong>Opening Hours:</strong> Mon-Fri 7am-8pm, Sat-Sun 8am-10pm</p>
        </div>
        <div class="contact-form slide-in">
            <h2>Send a Message</h2>
            <form id="contactForm">
                <div class="form-group">
                    <input type="text" id="name" placeholder=" " required>
                    <label for="name">Name</label>
                </div>
                <div class="form-group">
                    <input type="email" id="email" placeholder=" " required>
                    <label for="email">Email</label>
                </div>
                <div class="form-group">
                    <textarea id="message" placeholder=" " required></textarea>
                    <label for="message">Message</label>
                </div>
                <button type="submit" class="btn submit-btn">Submit</button>
            </form>
            <div id="formMessage" class="message"></div>
        </div>
    </section>

    <section id="conversion">
        <div class="slide-in">
            <h2>A Cafe Designed to Be Remembered.</h2>
            <p>Bring the luxury of NOIR ÉLAN CAFÉ to your brand with our premium website services.</p>
            <button class="btn">Get Your Demo</button>
        </div>
    </section>

    <footer>
        <div class="divider"></div>
        <h3>NOIR ÉLAN CAFÉ</h3>
        <p>Crafted in Detail. Served with Intention.</p>
    </footer>

    <script>
        // Intersection Observer for animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in, .slide-in').forEach(el => observer.observe(el));

        // Form validation
        const form = document.getElementById('contactForm');
        const messageDiv = document.getElementById('formMessage');

        form.addEventListener('submit', function(e) {
            e.preventDefault();
            const name = document.getElementById('name').value.trim();
            const email = document.getElementById('email').value.trim();
            const message = document.getElementById('message').value.trim();

            if (name === '' || email === '' || message === '') {
                messageDiv.textContent = 'Please fill in all fields.';
                messageDiv.className = 'message error';
                return;
            }

            const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            if (!emailRegex.test(email)) {
                messageDiv.textContent = 'Please enter a valid email address.';
                messageDiv.className = 'message error';
                return;
            }

            // Simulate form submission (no backend)
            messageDiv.textContent = 'Thank you for your message. We will get back to you soon.';
            messageDiv.className = 'message success';
            form.reset();
        });
    </script>
</body>
</html>
