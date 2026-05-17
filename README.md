<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>YOU-TECH AFRICA | Empowering Next-Gen Tech Innovators</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=Poppins:wght@700;900&display=swap" rel="stylesheet">
    <style>
        * {margin: 0;padding: 0;box-sizing: border-box;}
        html {scroll-behavior: smooth;}
        body {font-family: 'Inter', sans-serif;font-weight: 400;color: #1E293B;line-height: 1.5;background-color: #FFFFFF;}
        h1, h2, h3, h4 {font-family: 'Poppins', sans-serif;color: #1E3A8A;}
        a {text-decoration: none;transition: all 0.3s ease;}
        ul {list-style: none;}
        .container {max-width: 1200px;margin: 0 auto;padding: 0 24px;}
        .btn {display: inline-block;padding: 12px 24px;border-radius: 8px;font-weight: 600;cursor: pointer;transition: all 0.3s ease;border: none;text-align: center;}
        .btn:hover {transform: translateY(-2px);box-shadow: 0 8px 24px rgba(249, 115, 22, 0.3);}
        .btn-primary {background-color: #F97316;color: #FFFFFF;}
        .btn-outline {background-color: transparent;border: 2px solid #FFFFFF;color: #FFFFFF;}
        .btn:disabled {opacity: 0.6;cursor: not-allowed;transform: none;box-shadow: none;}
        section {padding: 80px 0;}

        header {position: sticky;top: 0;height: 80px;background: #FFFFFF;box-shadow: 0 2px 10px rgba(0,0,0,0.05);z-index: 1000;display: flex;align-items: center;}
        header .container {display: flex;justify-content: space-between;align-items: center;width: 100%;}
        .logo {font-size: 20px;font-weight: 700;color: #1E3A8A;font-family: 'Poppins', sans-serif;}
        .nav-links {display: flex;align-items: center;gap: 32px;}
        .nav-links a {font-size: 15px;color: #1E293B;font-weight: 500;}
        .nav-links a:hover {color: #F97316;}
        #menu-toggle {display: none;}
        .hamburger {display: none;cursor: pointer;font-size: 24px;color: #1E3A8A;}

        .hero {height: 600px;background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1522202176988-66273c2fd55f?w=1600') center/cover no-repeat;display: flex;align-items: center;padding: 0;}
        .hero-content {max-width: 600px;}
        .hero h1 {font-size: 48px;font-weight: 900;color: #FFFFFF;line-height: 1.2;margin-bottom: 20px;}
        .hero p {font-size: 18px;color: #E2E8F0;margin-bottom: 32px;}
        .hero-btns {display: flex;gap: 16px;}

        .who-we-are {background-color: #FFFFFF;}
        .grid-2 {display: grid;grid-template-columns: 1fr 1fr;gap: 60px;align-items: center;}
        .who-we-are h2 {font-size: 32px;margin-bottom: 16px;}
        .who-we-are p {color: #64748B;font-size: 16px;line-height: 1.7;margin-bottom: 20px;}
        .learn-more {color: #F97316;font-weight: 600;}
        .who-image {width: 100%;border-radius: 16px;display: block;}
        
        .programs {background-color: #F8FAFC;text-align: center;}
        .programs-header {margin-bottom: 48px;}
        .programs-header p {color: #64748B;}
        .grid-4 {display: grid;grid-template-columns: repeat(4, 1fr);gap: 24px;margin-bottom: 40px;}
        .program-card {background: #FFFFFF;padding: 32px 24px;border-radius: 12px;box-shadow: 0 4px 20px rgba(0,0,0,0.08);text-align: center;}
        .icon-box {width: 40px;height: 40px;background-color: #F97316;border-radius: 8px;margin: 0 auto 20px;}
        .program-card h3 {font-size: 18px;font-weight: 600;color: #1E293B;margin-bottom: 12px;}
        .program-card p {font-size: 14px;color: #64748B;}
        
        .stats {background-color: #1E3A8A;color: #FFFFFF;padding: 60px 0;text-align: center;}
        .stats-grid {display: grid;grid-template-columns: repeat(4, 1fr);gap: 20px;}
        .stat-item h3 {font-size: 40px;font-weight: 900;color: #FFFFFF;margin-bottom: 4px;}
        
        .testimonials {background-color: #FFFFFF;}
        .testimonials-grid {display: grid;grid-template-columns: 1fr 1fr;gap: 32px;margin-bottom: 32px;}
        .testimonial-card {background: #F8FAFC;padding: 32px;border-radius: 12px;border-left: 4px solid #F97316;}
        .testimonial-card p.quote {font-size: 16px;color: #1E293B;font-style: italic;margin-bottom: 16px;line-height: 1.7;}
        .testimonial-card p.author {font-size: 14px;color: #64748B;font-weight: 500;}
        .text-center {text-align: center;}
        
        .cta-banner {background-color: #F97316;padding: 60px 0;text-align: center;}
        .cta-banner h2 {color: #FFFFFF;font-size: 36px;margin-bottom: 24px;}
        .cta-btns {display: flex;justify-content: center;gap: 16px;}
        .cta-btns .btn-white {background: #FFFFFF;color: #F97316;}
        
        footer {background-color: #1E3A8A;padding: 60px 0 24px;color: #CBD5E1;}
        .footer-grid {display: grid;grid-template-columns: 1.5fr 1fr 1fr;gap: 40px;}
        .footer-grid h3, .footer-grid h4 {color: #FFFFFF;margin-bottom: 20px;}
        .footer-links li {margin-bottom: 12px;}
        .footer-links a {color: #CBD5E1;}
        .footer-links a:hover {color: #FFFFFF;}
        .footer-bottom {border-top: 1px solid rgba(255,255,255,0.1);padding-top: 24px;margin-top: 40px;text-align: center;font-size: 14px;}

        /* Modal + Form */
        .modal {display: none;position: fixed;inset: 0;background: rgba(0,0,0,0.6);align-items: center;justify-content: center;padding: 20px;z-index: 2000;}
        .modal.active {display: flex;}
        .modal-content {background: #fff;border-radius: 16px;padding: 32px;max-width: 560px;width: 100%;max-height: 90vh;overflow-y: auto;position: relative;}
        .modal-close {position: absolute;top: 12px;right: 12px;background: none;border: none;font-size: 28px;cursor: pointer;color: #64748B;}
        .modal h3 {margin-bottom: 16px;font-size: 24px;}
        .form-grid {display: grid;grid-template-columns: 1fr 1fr;gap: 16px;}
        .form-group {display: flex;flex-direction: column;gap: 6px;}
        .form-group.full {grid-column: 1 / -1;}
        label {font-size: 14px;font-weight: 500;color: #1E293B;}
        input, select, textarea {padding: 12px;border: 1px solid #CBD5E1;border-radius: 8px;font-family: 'Inter', sans-serif;font-size: 14px;}
        input:focus, select:focus, textarea:focus {outline: none;border-color: #F97316;box-shadow: 0 0 0 3px rgba(249,115,22,0.2);}
        
        /* Formspree states */
        .error {color: #dc2626;font-size: 12px;display: none;}
        .error.show {display: block;}
        .success-msg {background: #16a34a;color: #fff;padding: 14px 20px;border-radius: 8px;margin-bottom: 16px;display: none;text-align: center;}
        .success-msg.show {display: block;}
        .error-msg {background: #dc2626;color: #fff;padding: 14px 20px;border-radius: 8px;margin-bottom: 16px;display: none;}
        .error-msg.show {display: block;}

        @media (max-width: 1024px) {.grid-4 {grid-template-columns: repeat(2, 1fr);}}
        @media (max-width: 768px) {
            .hamburger {display: block;}
            .nav-links {display: none;position: absolute;top: 80px;left: 0;width: 100%;background: #FFFFFF;flex-direction: column;padding: 24px;gap: 20px;box-shadow: 0 10px 15px rgba(0,0,0,0.1);}
            #menu-toggle:checked ~ .nav-links {display: flex;}
            .hero {text-align: center;}
            .hero h1 {font-size: 32px;}
            .hero-btns {flex-direction: column;align-items: center;}
            .grid-2, .grid-4, .stats-grid, .testimonials-grid, .footer-grid {grid-template-columns: 1fr;}
            .form-grid {grid-template-columns: 1fr;}
            .cta-btns {flex-direction: column;padding: 0 20px;}
        }
    </style>
</head>
<body>

    <header>
        <div class="container">
            <div class="logo">YOU-TECH AFRICA</div>
            <input type="checkbox" id="menu-toggle">
            <label for="menu-toggle" class="hamburger">☰</label>
            <nav class="nav-links">
                <a href="#">Home</a>
                <a href="#about">About</a>
                <a href="#programs">Programs</a>
                <a href="#impact">Impact</a>
                <a href="#testimonials">Testimonials</a>
                <a href="#contact">Contact</a>
                <button class="btn btn-primary" data-open-modal>Apply Now</button>
            </nav>
        </div>
    </header>

    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Empowering Africa's Next Generation of Tech Innovators</h1>
                <p>We equip young Africans with the skills, experience, and mentorship needed to thrive in technology and innovation.</p>
                <div class="hero-btns">
                    <button class="btn btn-primary" data-open-modal>Join Our Community</button>
                    <a href="#programs" class="btn btn-outline">Explore Our Programs</a>
                </div>
            </div>
        </div>
    </section>

    <section id="about" class="who-we-are">
        <div class="container">
            <div class="grid-2">
                <div>
                    <h2>Who We Are</h2>
                    <p>You-Tech Africa is a tech-focused capacity-building organization dedicated to equipping young Africans (16-35) with practical digital skills, mentorship, and real-world experience.</p>
                    <a href="#" class="learn-more">Learn More →</a>
                </div>
                <div>
                    <img src="https://images.unsplash.com/photo-1523240795612-9a054b0db644?w=600" alt="Students collaborating" class="who-image" loading="lazy">
                </div>
            </div>
        </div>
    </section>

    <section id="programs" class="programs">
        <div class="container">
            <div class="programs-header">
                <h2>Our Programs</h2>
                <p>Comprehensive training designed to build real-world tech skills.</p>
            </div>
            <div class="grid-4">
                <div class="program-card"><div class="icon-box"></div><h3>Mini Internship Program</h3><p>Hands-on projects with real-world applications</p></div>
                <div class="program-card"><div class="icon-box"></div><h3>Training & Workshops</h3><p>Learn in-demand technical and soft skills</p></div>
                <div class="program-card"><div class="icon-box"></div><h3>Mentorship & Coaching</h3><p>One-on-one guidance from experienced professionals</p></div>
                <div class="program-card"><div class="icon-box"></div><h3>Community Engagement</h3><p>Connect and grow with like-minded peers</p></div>
            </div>
            <button class="btn btn-primary" data-open-modal>View All Programs</button>
        </div>
    </section>

    <section id="impact" class="stats">
        <div class="container">
            <div class="stats-grid">
                <div class="stat-item"><h3>300+</h3><p>Students Trained</p></div>
                <div class="stat-item"><h3>100+</h3><p>Mentors Paired</p></div>
                <div class="stat-item"><h3>80%+</h3><p>Career Advancement Rate</p></div>
                <div class="stat-item"><h3>Growing</h3><p>Community Across Africa</p></div>
            </div>
        </div>
    </section>

    <section id="testimonials" class="testimonials">
        <div class="container">
            <h2 class="text-center" style="margin-bottom: 48px;">What Our Students Say</h2>
            <div class="testimonials-grid">
                <div class="testimonial-card"><p class="quote">"You-Tech Africa gave me more than skills, it gave me confidence to create and lead in tech."</p><p class="author">— Aisha, UI/UX Intern</p></div>
                <div class="testimonial-card"><p class="quote">"The mentorship and hands-on projects prepared me for the real tech world. I secured a paid role at a fintech after 3 months."</p><p class="author">— Chukwu, Frontend Developer Intern</p></div>
            </div>
            <div class="text-center"><a href="#" class="learn-more">Read More Stories →</a></div>
        </div>
    </section>

    <section id="apply" class="cta-banner">
        <div class="container">
            <h2>Be part of Africa's tech revolution.</h2>
            <div class="cta-btns">
                <button class="btn btn-white" data-open-modal>Apply Now</button>
                <a href="#" class="btn btn-outline">Join Our WhatsApp Community</a>
            </div>
        </div>
    </section>

    <footer id="contact">
        <div class="container">
            <div class="footer-grid">
                <div><h3>YOU-TECH AFRICA</h3><p>Empowering the next generation of African tech leaders through education and opportunity.</p></div>
                <div><h4>Quick Links</h4><ul class="footer-links"><li><a href="#about">About Us</a></li><li><a href="#programs">Programs</a></li><li><a href="#impact">Impact</a></li><li><a href="#contact">Contact</a></li></ul></div>
                <div><h4>Contact</h4><p>hello@you-techafrica.org</p></div>
            </div>
            <div class="footer-bottom"><p>&copy; 2026 YOU-TECH AFRICA. All rights reserved.</p></div>
        </div>
    </footer>

    <!-- Modal Form -->
    <div class="modal" id="applyModal" role="dialog" aria-modal="true" aria-labelledby="modalTitle">
        <div class="modal-content">
            <button class="modal-close" aria-label="Close">&times;</button>
            <h3 id="modalTitle">Apply to YOU-TECH AFRICA</h3>
            
            <div data-fs-success class="success-msg">We've gotten your application. We'll get to you within 48 hrs</div>
            <div data-fs-error class="error-msg">Something went wrong. Please try again.</div>

            <form id="applyForm">
                <div class="form-grid">
                    <div class="form-group">
                        <label for="fullName">Full Name</label>
                        <input type="text" id="fullName" name="name" data-fs-field required>
                        <span class="error" data-fs-error="name">Name is required</span>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" name="email" data-fs-field required>
                        <span class="error" data-fs-error="email">Valid email required</span>
                    </div>
                    <div class="form-group">
                        <label for="phone">Phone</label>
                        <input type="tel" id="phone" name="phone" data-fs-field required>
                        <span class="error" data-fs-error="phone">Phone is required</span>
                    </div>
                    <div class="form-group">
                        <label for="program">Program Interest</label>
                        <select id="program" name="program" data-fs-field required>
                            <option value="">Select</option>
                            <option>Mini Internship Program</option>
                            <option>Training & Workshops</option>
                            <option>Mentorship & Coaching</option>
                            <option>Community Engagement</option>
                        </select>
                        <span class="error" data-fs-error="program">Select a program</span>
                    </div>
                    <div class="form-group full">
                        <label for="message">Why do you want to join?</label>
                        <textarea id="message" name="message" rows="4" data-fs-field required></textarea>
                        <span class="error" data-fs-error="message">Message is required</span>
                    </div>
                </div>
                <button type="submit" class="btn btn-primary" data-fs-submit-btn style="width:100%;margin-top:16px;">Submit Application</button>
            </form>
        </div>
    </div>

<script>
// Modal Logic
const modal = document.getElementById('applyModal');
const openBtns = document.querySelectorAll('[data-open-modal]');
const closeBtn = document.querySelector('.modal-close');

openBtns.forEach(btn => btn.addEventListener('click', () => {
    modal.classList.add('active');
    document.body.style.overflow = 'hidden';
    document.getElementById('fullName').focus();
}));

closeBtn.addEventListener('click', closeModal);
modal.addEventListener('click', e => {if(e.target === modal) closeModal();});
document.addEventListener('keydown', e => {if(e.key === 'Escape') closeModal();});

function closeModal() {
    modal.classList.remove('active');
    document.body.style.overflow = '';
}

// Init Formspree AJAX
window.formspree = window.formspree || function () { (formspree.q = formspree.q || []).push(arguments); };
formspree('initForm', { 
    formElement: '#applyForm', 
    formId: 'mkoykzgp',
    onSuccess: () => {
        document.getElementById('applyForm').reset();
        setTimeout(closeModal, 3000);
    }
});
</script>
<script src="https://unpkg.com/@formspree/ajax@1" defer></script>
</body>
</html>
