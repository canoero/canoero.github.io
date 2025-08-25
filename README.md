<!-- 
    DJ ELITE FUNNEL V4 - WEBFLOW & SYSTEME.IO EDITION
    
    HOW TO USE IN WEBFLOW:
    1. In your Webflow project, add an "HTML Embed" element to your page. Make it the only element on the page.
    2. Open the HTML Embed editor.
    3. Copy this ENTIRE file and paste it into the Webflow HTML Embed editor.
    4. Save and close the editor.
    5. Find all instances of the link "#systeme-io-payment-link" in the code and replace it with your actual Systeme.io payment page URL.
    6. Publish your Webflow site.
-->

<style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap');

    :root {
        --bg-dark: #050507;
        --bg-card: #111115;
        --text-light: #9E9EAD;
        --text-white: #FFFFFF;
        --accent-primary: #00F5A0;
        --accent-secondary: #6C3B9F;
        --border-color: rgba(255, 255, 255, 0.1);
        --font-sans: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
        --gradient-main: linear-gradient(135deg, var(--accent-primary) 0%, var(--accent-secondary) 100%);
    }

    /* BASE & TYPOGRAPHY */
    .dj-v4-container, .dj-v4-container * {
        font-family: var(--font-sans);
        box-sizing: border-box;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
    }
    .dj-v4-container {
        background-color: var(--bg-dark);
        color: var(--text-light);
        line-height: 1.7;
        padding: 0;
        margin: 0;
        overflow-x: hidden;
    }
    .dj-v4-container .container { max-width: 1180px; margin: 0 auto; padding: 0 30px; }
    .dj-v4-container .section { padding: 120px 0; position: relative; }
    .dj-v4-container .text-center { text-align: center; }

    .dj-v4-container h1, .dj-v4-container h2, .dj-v4-container h3, .dj-v4-container h4 { color: var(--text-white); font-weight: 800; line-height: 1.2; }
    .dj-v4-container .heading-xl { font-size: clamp(3.5rem, 7vw, 6rem); margin-bottom: 1.5rem; letter-spacing: -0.03em; }
    .dj-v4-container .heading-lg { font-size: clamp(2.5rem, 5vw, 4rem); margin-bottom: 2rem; letter-spacing: -0.02em; }
    .dj-v4-container .heading-md { font-size: 1.75rem; margin-bottom: 1rem; }
    .dj-v4-container .p-large { font-size: 1.25rem; max-width: 720px; margin: 0 auto 2.5rem; }
    .dj-v4-container .text-gradient { background: var(--gradient-main); background-clip: text; -webkit-background-clip: text; -webkit-text-fill-color: transparent; }

    /* BUTTON */
    .dj-v4-container .btn {
        display: inline-block;
        background: var(--gradient-main);
        color: var(--text-white);
        padding: 20px 40px;
        border-radius: 50px;
        font-weight: 700;
        font-size: 1.1rem;
        text-decoration: none;
        cursor: pointer;
        border: none;
        transition: transform 0.3s ease, box-shadow 0.3s ease;
        box-shadow: 0 10px 30px rgba(0, 245, 160, 0.2);
    }
    .dj-v4-container .btn:hover { transform: translateY(-5px) scale(1.05); box-shadow: 0 15px 40px rgba(0, 245, 160, 0.3); }

    /* HERO */
    .dj-v4-container .hero { padding: 180px 0 120px; min-height: 100vh; display: flex; align-items: center; }
    .dj-v4-container .hero-sub-badge {
        display: inline-block;
        border: 1px solid var(--border-color);
        background: rgba(255,255,255,0.05);
        color: var(--text-light);
        padding: 10px 20px;
        border-radius: 20px;
        margin-top: 2.5rem;
        font-size: 0.9rem;
    }

    /* LOGO STRIP */
    .dj-v4-container .logo-strip { padding: 40px 0; border-top: 1px solid var(--border-color); border-bottom: 1px solid var(--border-color); }
    .dj-v4-container .logo-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); gap: 40px; align-items: center; justify-items: center; }
    .dj-v4-container .logo-grid img { max-height: 25px; filter: grayscale(1) brightness(10); opacity: 0.6; transition: all 0.3s ease; }

    /* EPIPHANY BRIDGE (STORY) SECTION */
    .dj-v4-container .story-grid { display: grid; grid-template-columns: 300px 1fr; gap: 60px; align-items: center; margin-top: 5rem; }
    @media (max-width: 992px) { .dj-v4-container .story-grid { grid-template-columns: 1fr; text-align: center; } }
    .dj-v4-container .creator-image { width: 100%; max-width: 300px; border-radius: 20px; border: 2px solid var(--border-color); }
    .dj-v4-container .story-quote {
        font-size: 1.5rem;
        font-style: italic;
        color: var(--text-white);
        border-left: 3px solid var(--accent-primary);
        padding-left: 2rem;
        margin: 2rem 0;
    }

    /* VALUE STACK SECTION */
    .dj-v4-container .stack-section { background: var(--bg-card); }
    .dj-v4-container .stack-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 30px; margin-top: 5rem; }
    @media (max-width: 768px) { .dj-v4-container .stack-grid { grid-template-columns: 1fr; } }
    .dj-v4-container .stack-item {
        background: var(--bg-dark);
        border: 1px solid var(--border-color);
        border-radius: 15px;
        padding: 2rem;
        display: flex;
        align-items: flex-start;
        gap: 20px;
    }
    .dj-v4-container .stack-icon { font-size: 1.5rem; color: var(--accent-primary); line-height: 1; margin-top: 5px; }
    .dj-v4-container .stack-value { font-size: 0.9rem; color: var(--accent-primary); font-weight: 600; }
    .dj-v4-container .total-value-box {
        background: var(--bg-dark);
        border: 2px solid var(--accent-primary);
        border-radius: 20px;
        padding: 2rem;
        margin-top: 3rem;
        text-align: center;
    }

    /* PRICING */
    .dj-v4-container .pricing-card {
        background: var(--bg-card);
        border: 1px solid var(--border-color);
        border-radius: 25px;
        padding: 3rem;
        max-width: 700px;
        margin: 5rem auto 0;
        box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
    }
    .dj-v4-container .price { font-size: 6rem; font-weight: 800; color: var(--text-white); margin: 1rem 0; line-height: 1; }
    .dj-v4-container .price-original { font-size: 2rem; color: var(--text-light); text-decoration: line-through; margin-left: 1rem; }
    .dj-v4-container .guarantee-box {
        display: flex;
        gap: 20px;
        align-items: center;
        background: rgba(0, 245, 160, 0.05);
        border: 1px solid rgba(0, 245, 160, 0.2);
        border-radius: 15px;
        padding: 1.5rem;
        margin-top: 2.5rem;
    }
    .dj-v4-container .guarantee-icon { font-size: 3rem; }

    /* TESTIMONIALS */
    .dj-v4-container .testimonial-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 30px; margin-top: 5rem; }
    .dj-v4-container .testimonial-card {
        background: var(--bg-card);
        border: 1px solid var(--border-color);
        border-radius: 15px;
        padding: 2rem;
    }
    .dj-v4-container .testimonial-author { display: flex; align-items: center; margin-top: 1.5rem; gap: 15px; }
    .dj-v4-container .author-image { width: 50px; height: 50px; border-radius: 50%; object-fit: cover; border: 2px solid var(--accent-primary); }
    .dj-v4-container .author-name { font-weight: bold; color: var(--text-white); }
    .dj-v4-container .testimonial-result { font-weight: 600; color: var(--accent-primary); }

    /* FAQ */
    .dj-v4-container .faq-grid { max-width: 800px; margin: 5rem auto 0; }
    .dj-v4-container .faq-item { border-bottom: 1px solid var(--border-color); padding: 1.5rem 0; }
    .dj-v4-container .faq-question { display: flex; justify-content: space-between; align-items: center; cursor: pointer; font-size: 1.2rem; font-weight: 600; color: var(--text-white); }
    .dj-v4-container .faq-icon { font-size: 1.5rem; transition: transform 0.3s ease; color: var(--accent-primary); }
    .dj-v4-container .faq-answer { max-height: 0; overflow: hidden; transition: max-height 0.5s ease, padding-top 0.5s ease; }
    .dj-v4-container .faq-item.active .faq-answer { padding-top: 1rem; }
    .dj-v4-container .faq-item.active .faq-icon { transform: rotate(45deg); }

    /* FOOTER */
    .dj-v4-container .footer { background: #000; padding: 60px 0; border-top: 1px solid var(--border-color); text-align: center; }

    /* GSAP ANIMATION PREP */
    .g-fade-up { opacity: 0; transform: translateY(40px); }
    .g-fade-in { opacity: 0; }
    .g-clip-text { -webkit-text-fill-color: var(--bg-dark); }

</style>

<div class="dj-v4-container">

    <main>
        <!-- ======================= -->
        <!-- 1. HERO (THE HOOK)      -->
        <!-- ======================= -->
        <section class="hero text-center">
            <div class="container">
                <h1 class="heading-xl g-clip-text">Stop DJing for Free.</h1>
                <p class="p-large g-fade-up">A shocking truth: The world's highest-paid DJs aren't always the most skilled. They're the best marketed. We cracked their code. This is the system that gets you booked and paid like a pro, even if you don't have connections.</p>
                <div class="g-fade-up">
                    <a href="#systeme-io-payment-link" class="btn">Get The Pro Toolkit - $47</a>
                    <p class="hero-sub-badge">Join 1,200+ DJs Who Transformed Their Hobby Into a Career</p>
                </div>
            </div>
        </section>

        <div class="logo-strip">
            <div class="container g-fade-in">
                <p class="text-center" style="margin-bottom: 2rem; font-weight: bold; color: var(--text-light); text-transform: uppercase; font-size: 0.8rem; letter-spacing: 1px;">Our Members Have Been Featured In</p>
                <div class="logo-grid">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e4/Mixmag_logo.svg/1280px-Mixmag_logo.svg.png" alt="Mixmag Logo">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/35/DJ_Mag_logo.svg/1280px-DJ_Mag_logo.svg.png" alt="DJ Mag Logo">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Resident_Advisor_logo.svg/1280px-Resident_Advisor_logo.svg.png" alt="Resident Advisor Logo">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f1/Beatport_logo.svg/1280px-Beatport_logo.svg.png" alt="Beatport Logo">
                </div>
            </div>
        </div>

        <!-- =================================== -->
        <!-- 2. STORY (THE EPIPHANY BRIDGE)    -->
        <!-- =================================== -->
        <section class="section">
            <div class="container">
                <div class="text-center">
                    <h2 class="heading-lg g-fade-up">I Was Just Like You... Stuck.</h2>
                    <p class="p-large g-fade-up">Spending thousands on gear and countless hours practicing, only to play for my friends or for drink tickets. I thought talent was enough. I was wrong.</p>
                </div>
                <div class="story-grid">
                    <div class="g-fade-up">
                        <img src="https://images.unsplash.com/photo-1517245386807-bb43f82c33c4?q=80&w=2070&auto=format&fit=crop" alt="Course Creator" class="creator-image">
                    </div>
                    <div class="g-fade-up">
                        <p>For years, I sent emails that got ignored. I watched less talented DJs get the gigs I wanted. The frustration was immense. I almost quit.</p>
                        <p class="story-quote">Then I had an epiphany: The problem wasn't my mixing. It was my marketing. I stopped acting like an artist and started acting like a business.</p>
                        <p>I spent a year studying what top-tier DJs and promoters *actually* look for. I built a system—a professional press kit, outreach scripts that got replies, and a simple way to manage bookings. Within 60 days, I was booked solid at triple my old rate. This toolkit contains that exact system.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- =================================== -->
        <!-- 3. OFFER (THE VALUE STACK)        -->
        <!-- =================================== -->
        <section class="section stack-section">
            <div class="container text-center">
                <h2 class="heading-lg g-fade-up">The Complete <span class="text-gradient">Pro DJ Toolkit</span></h2>
                <p class="p-large g-fade-up">This isn't a course. It's a "business-in-a-box" for DJs. You get the exact, field-tested assets we use to book high-paying gigs.</p>
                <div class="stack-grid">
                    <div class="stack-item g-fade-up">
                        <div class="stack-icon">📋</div>
                        <div>
                            <h4 class="heading-md">Pro Press Kit Templates</h4>
                            <p>Stunning, editable templates (Canva & Photoshop) that make you look like a seasoned pro from the first email. <span class="stack-value">(Value: $197)</span></p>
                        </div>
                    </div>
                    <div class="stack-item g-fade-up">
                        <div class="stack-icon">💬</div>
                        <div>
                            <h4 class="heading-md">The "Reply-Guaranteed" Script Bible</h4>
                            <p>50+ copy-paste scripts for emails, DMs, and follow-ups that get replies from promoters and bookers. <span class="stack-value">(Value: $147)</span></p>
                        </div>
                    </div>
                    <div class="stack-item g-fade-up">
                        <div class="stack-icon">💼</div>
                        <div>
                            <h4 class="heading-md">Booking & Invoice System</h4>
                            <p>Simple templates for contracts, invoices, and technical riders that protect you and make you look professional. <span class="stack-value">(Value: $97)</span></p>
                        </div>
                    </div>
                    <div class="stack-item g-fade-up">
                        <div class="stack-icon">🌐</div>
                        <div>
                            <h4 class="heading-md">The Black Book of Contacts</h4>
                            <p>A curated list of 200+ venues, promoters, and booking agents in major cities who are actively looking for DJs. <span class="stack-value">(Value: $297)</span></p>
                        </div>
                    </div>
                </div>
                <div class="total-value-box g-fade-up">
                    <h3 class="heading-lg" style="margin-bottom: 0.5rem;">Total Value: <span style="text-decoration: line-through;">$738</span></h3>
                    <p>...but you're not paying that today.</p>
                </div>
            </div>
        </section>

        <!-- =================================== -->
        <!-- 4. PRICING & RISK REVERSAL        -->
        <!-- =================================== -->
        <section id="pricing" class="section">
            <div class="container text-center">
                <h2 class="heading-lg g-fade-up">Get Instant Access Today</h2>
                <p class="p-large g-fade-up">For a limited time, get the entire Pro DJ Toolkit for less than the price of a single bad gig.</p>
                
                <div class="pricing-card g-fade-up">
                    <p>You Pay Only:</p>
                    <div>
                        <span class="price">$47</span>
                        <span class="price-original">$738</span>
                    </div>
                    <p style="font-weight: 700; color: var(--accent-primary);">A Single, One-Time Payment for Lifetime Access</p>
                    <div style="margin: 2rem 0;">
                        <a href="#systeme-io-payment-link" class="btn" style="width: 100%; font-size: 1.3rem; padding: 24px;">Claim My 93% Discount Now</a>
                    </div>
                    <div class="guarantee-box">
                        <div class="guarantee-icon">🛡️</div>
                        <div>
                            <h4 class="heading-md" style="margin-bottom: 0.5rem;">The "Book a Gig" 30-Day Guarantee</h4>
                            <p style="font-size: 0.9rem;">Use our system. If you don't book at least one paid gig within 30 days that more than covers this small investment, email us and we'll send you a full refund. No questions asked.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- =================================== -->
        <!-- 5. SOCIAL PROOF (TESTIMONIALS)    -->
        <!-- =================================== -->
        <section class="section" style="background: var(--bg-card);">
            <div class="container">
                <div class="text-center">
                    <h2 class="heading-lg g-fade-up">From Zero to Hero: Real Results</h2>
                    <p class="p-large g-fade-up">This system works. But don't take our word for it.</p>
                </div>
                <div class="testimonial-grid">
                    <div class="testimonial-card g-fade-up">
                        <p>"I was skeptical. 2 weeks after using the press kit and one email script, I landed a residency at a club I'd been trying to get into for a year. This is the real deal."</p>
                        <div class="testimonial-author">
                            <img src="https://images.unsplash.com/photo-1560250097-0b93528c311a?q=80&w=150&h=150&auto=format&fit=crop" alt="Testimonial author" class="author-image">
                            <div>
                                <p class="author-name">Chris P.</p>
                                <p class="testimonial-result">Gig Rate: $100 ➔ $500/night</p>
                            </div>
                        </div>
                    </div>
                    <div class="testimonial-card g-fade-up">
                        <p>"The 'Black Book' was worth the price alone. I was targeting the wrong venues. Used the contact list and scripts, and booked 3 corporate events in one month. My income has quadrupled."</p>
                        <div class="testimonial-author">
                            <img src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?q=80&w=150&h=150&auto=format&fit=crop" alt="Testimonial author" class="author-image">
                            <div>
                                <p class="author-name">Sofia Rodriguez</p>
                                <p class="testimonial-result">Monthly Income: $800 ➔ $3,500+</p>
                            </div>
                        </div>
                    </div>
                    <div class="testimonial-card g-fade-up">
                        <p>"Before this, I had no idea how to write a professional contract or rider. The templates gave me instant credibility and the confidence to ask for what I'm worth. Game-changer."</p>
                        <div class="testimonial-author">
                            <img src="https://images.unsplash.com/photo-1557862921-37829c790f19?q=80&w=150&h=150&auto=format&fit=crop" alt="Testimonial author" class="author-image">
                            <div>
                                <p class="author-name">Marco V.</p>
                                <p class="testimonial-result">Booked first-ever paid festival slot.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- =================================== -->
        <!-- 6. FAQ (OBJECTION HANDLING)       -->
        <!-- =================================== -->
        <section id="faq" class="section">
            <div class="container">
                <div class="text-center">
                    <h2 class="heading-lg g-fade-up">Your Questions, Answered.</h2>
                </div>
                <div class="faq-grid">
                    <div class="faq-item g-fade-up">
                        <div class="faq-question"><span>Is this really worth it if I'm just starting?</span><span class="faq-icon">+</span></div>
                        <div class="faq-answer"><p>This is *especially* for you. It's designed to help you skip years of trial-and-error (and playing for free). Looking professional from day one is the fastest way to get paid, even if your skills are still developing.</p></div>
                    </div>
                    <div class="faq-item g-fade-up">
                        <div class="faq-question"><span>What if I live in a small town?</span><span class="faq-icon">+</span></div>
                        <div class="faq-answer"><p>The principles of professional marketing are universal. This system works for booking local bars, weddings, corporate events, and even online DJ sets. The "Black Book" also includes strategies for finding key contacts in any city, no matter the size.</p></div>
                    </div>
                    <div class="faq-item g-fade-up">
                        <div class="faq-question"><span>Is this a recurring subscription?</span><span class="faq-icon">+</span></div>
                        <div class="faq-answer"><p>No. It is a one-time payment of $47. You get lifetime access to all the current materials and all future updates, forever. No hidden fees, no upsells inside.</p></div>
                    </div>
                    <div class="faq-item g-fade-up">
                        <div class="faq-question"><span>What format are the files in?</span><span class="faq-icon">+</span></div>
                        <div class="faq-answer"><p>The templates are provided in the most popular, easy-to-use formats: Canva, Adobe Photoshop, and Microsoft Word/Google Docs. The guides and scripts are in PDF format. Everything is accessible on any device.</p></div>
                    </div>
                </div>
            </div>
        </section>

        <!-- =================================== -->
        <!-- 7. FINAL CTA                      -->
        <!-- =================================== -->
        <section class="section" style="background: var(--bg-card);">
            <div class="container text-center">
                <h2 class="heading-lg g-fade-up">Two Paths Lie Before You...</h2>
                <p class="p-large g-fade-up">
                    <strong>Path 1:</strong> Keep doing what you're doing. Hope that one day your talent gets discovered. Spend another year playing for exposure.<br><br>
                    <strong>Path 2:</strong> Take the shortcut. Use a proven system, look like a pro from day one, and start getting the paid gigs you deserve. The choice is yours.
                </p>
                <div class="g-fade-up">
                    <a href="#systeme-io-payment-link" class="btn" style="font-size: 1.3rem; padding: 24px;">Yes, I'm Ready to Go Pro - Only $47</a>
                    <p style="margin-top: 1.5rem; font-size: 0.9rem;">🛡️ 100% Risk-Free Guarantee • ⚡ Instant Access</p>
                </div>
            </div>
        </section>

    </main>

    <footer class="footer">
        <div class="container">
            <p style="font-size: 1.5rem; font-weight: 700; color: var(--text-white);">DJ Elite</p>
            <p>&copy; 2025 DJ Elite. All Rights Reserved. This site is not affiliated with Facebook or any Facebook entity.</p>
        </div>
    </footer>

</div>

<!-- GSAP Animation Library -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>

<script>
function initDjV4() {
    // Register GSAP plugins
    gsap.registerPlugin(ScrollTrigger);

    // --- HERO ANIMATION ---
    const heroTimeline = gsap.timeline({ defaults: { ease: 'power3.out', duration: 1 } });
    
    // Animate text reveal
    const heroHeading = document.querySelector('.dj-v4-container .heading-xl');
    if(heroHeading) {
        heroTimeline.to(heroHeading, { 
            '--bg-dark': 'transparent', // Animate CSS variable to reveal text
            duration: 1.5
        })
        .from('.dj-v4-container .text-gradient', {
            backgroundPosition: '200% 0%',
            ease: 'power3.inOut',
            duration: 1.5
        }, "-=1.5")
        .from('.dj-v4-container .p-large.g-fade-up', { y: 30, opacity: 0, duration: 0.8 }, "-=1")
        .from('.dj-v4-container .g-fade-up .btn', { y: 30, opacity: 0, duration: 0.8 }, "-=0.6")
        .from('.dj-v4-container .hero-sub-badge', { y: 30, opacity: 0, duration: 0.8 }, "-=0.6");
    }

    // --- SCROLL-TRIGGERED ANIMATIONS ---
    const fadeUpElements = gsap.utils.toArray('.dj-v4-container .g-fade-up');
    fadeUpElements.forEach(el => {
        gsap.from(el, {
            scrollTrigger: {
                trigger: el,
                start: 'top 85%',
                toggleActions: 'play none none none'
            },
            opacity: 0,
            y: 50,
            duration: 1,
            ease: 'power3.out'
        });
    });
    
    const fadeInElements = gsap.utils.toArray('.dj-v4-container .g-fade-in');
    fadeInElements.forEach(el => {
        gsap.from(el, {
            scrollTrigger: {
                trigger: el,
                start: 'top 85%',
                toggleActions: 'play none none none'
            },
            opacity: 0,
            duration: 1.5,
            ease: 'power1.inOut'
        });
    });

    // Staggered animation for stack items
    gsap.from(".dj-v4-container .stack-item.g-fade-up", {
        scrollTrigger: {
            trigger: ".dj-v4-container .stack-grid",
            start: "top 80%",
            toggleActions: 'play none none none'
        },
        duration: 0.8,
        opacity: 0,
        y: 50,
        stagger: 0.2,
        ease: "power3.out"
    });

    // --- FAQ TOGGLE ---
    const faqItems = document.querySelectorAll('.dj-v4-container .faq-item');
    faqItems.forEach(item => {
        const question = item.querySelector('.faq-question');
        const answer = item.querySelector('.faq-answer');
        question.addEventListener('click', () => {
            const isActive = item.classList.contains('active');
            
            // Close all other items
            faqItems.forEach(i => {
                if (i !== item && i.classList.contains('active')) {
                    i.classList.remove('active');
                    gsap.to(i.querySelector('.faq-answer'), { maxHeight: 0, paddingTop: 0, duration: 0.4, ease: 'power2.inOut' });
                }
            });

            // Toggle current item
            item.classList.toggle('active');
            if (item.classList.contains('active')) {
                gsap.to(answer, { maxHeight: answer.scrollHeight, paddingTop: '1rem', duration: 0.5, ease: 'power2.out' });
            } else {
                gsap.to(answer, { maxHeight: 0, paddingTop: 0, duration: 0.4, ease: 'power2.inOut' });
            }
        });
    });
}

// Using a timeout to ensure Webflow/Systeme.io has finished its own rendering
setTimeout(initDjV4, 500);
</script>

