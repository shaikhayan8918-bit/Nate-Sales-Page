# Nate-sales-page
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RadicalYT - Scale Your YouTube Channel Into a Full-Time Business</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        html, body {
            overflow-x: hidden;
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            line-height: 1.6;
            color: #fff;
            background: #0a0a0a;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Background Animations */
        .bg-animation {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            overflow: hidden;
        }
        
        .bg-gradient {
            position: absolute;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle at 20% 50%, rgba(255, 0, 87, 0.1) 0%, transparent 50%),
                        radial-gradient(circle at 80% 20%, rgba(0, 149, 255, 0.1) 0%, transparent 50%),
                        radial-gradient(circle at 40% 80%, rgba(255, 195, 0, 0.1) 0%, transparent 50%);
            animation: float 20s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translate(-50%, -50%) rotate(0deg); }
            50% { transform: translate(-50%, -50%) rotate(180deg); }
        }
        
        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            padding: 100px 0;
        }
        
        .preheader {
            background: linear-gradient(135deg, #ff0057, #0095ff);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 600;
            font-size: 14px;
            letter-spacing: 2px;
            text-transform: uppercase;
            text-align: center;
            margin-bottom: 20px;
            opacity: 0;
            animation: slideUp 1s ease 0.2s forwards;
        }
        
        .hero h1 {
            font-size: clamp(48px, 8vw, 80px);
            font-weight: 900;
            line-height: 1.1;
            text-align: center;
            margin-bottom: 30px;
            opacity: 0;
            animation: slideUp 1s ease 0.4s forwards;
        }
        
        .hero h1 span.highlight {
            background: linear-gradient(135deg, #ff0057, #0095ff, #ffc300);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-size: 200% 200%;
            animation: gradientShift 3s ease-in-out infinite;
        }
        
        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        .subheader {
            font-size: clamp(20px, 3vw, 24px);
            color: #b0b0b0;
            text-align: center;
            margin-bottom: 40px;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            opacity: 0;
            animation: slideUp 1s ease 0.6s forwards;
        }
        
        .vsl-container {
            text-align: center;
            margin: 50px 0;
            opacity: 0;
            animation: slideUp 1s ease 0.8s forwards;
        }
        
        .vsl-icon {
            display: inline-block;
            position: relative;
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background: linear-gradient(135deg, #ff0057, #0095ff);
            cursor: pointer;
            transition: all 0.3s ease;
            margin-bottom: 15px;
        }
        
        .vsl-icon:hover {
            transform: scale(1.1);
            box-shadow: 0 20px 40px rgba(255, 0, 87, 0.3);
        }
        
        .vsl-icon::before {
            content: "▶";
            position: absolute;
            top: 50%;
            left: 55%;
            transform: translate(-50%, -50%);
            font-size: 40px;
            color: white;
        }
        
        .vsl-text {
            font-size: 18px;
            color: #fff;
            font-weight: 600;
            margin-bottom: 50px;
        }
        
        .cta-primary {
            display: inline-block;
            background: linear-gradient(135deg, #ff0057, #0095ff);
            color: white;
            padding: 20px 40px;
            font-size: 20px;
            font-weight: 700;
            text-decoration: none;
            border-radius: 50px;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
            box-shadow: 0 10px 30px rgba(255, 0, 87, 0.3);
        }
        
        .cta-primary:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(255, 0, 87, 0.5);
        }
        
        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        /* Section Styling */
        .section {
            padding: 100px 0;
            position: relative;
        }
        
        .section h2 {
            font-size: clamp(36px, 6vw, 56px);
            font-weight: 800;
            margin-bottom: 40px;
            text-align: center;
            line-height: 1.2;
        }
        
        .section-content {
            max-width: 900px;
            margin: 0 auto;
            font-size: 18px;
            line-height: 1.8;
        }
        
        .section-content p {
            margin-bottom: 25px;
            color: #d0d0d0;
        }
        
        .highlight-text {
            background: linear-gradient(135deg, #ff0057, #0095ff);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 700;
        }
        
        /* Problem Section */
        .problem-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 50px 0;
        }
        
        .problem-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 30px;
            transition: all 0.3s ease;
        }
        
        .problem-card:hover {
            transform: translateY(-10px);
            border-color: rgba(255, 0, 87, 0.5);
            box-shadow: 0 20px 40px rgba(255, 0, 87, 0.1);
        }
        
        .problem-icon {
            font-size: 48px;
            margin-bottom: 20px;
        }
        
        /* Bullets */
        .benefits-list {
            list-style: none;
            margin: 40px 0;
        }
        
        .benefits-list li {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 25px;
            margin-bottom: 20px;
            font-size: 18px;
            position: relative;
            transition: all 0.3s ease;
        }
        
        .benefits-list li:hover {
            transform: translateX(10px);
            border-color: rgba(0, 149, 255, 0.5);
        }
        
        .benefits-list li::before {
            content: "✓";
            position: absolute;
            left: -10px;
            top: 50%;
            transform: translateY(-50%);
            background: linear-gradient(135deg, #ff0057, #0095ff);
            color: white;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }
        
        /* Stats */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin: 50px 0;
        }
        
        .stat-card {
            text-align: center;
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 40px 20px;
        }
        
        .stat-number {
            font-size: 48px;
            font-weight: 900;
            background: linear-gradient(135deg, #ff0057, #0095ff);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            display: block;
        }
        
        .stat-label {
            font-size: 16px;
            color: #b0b0b0;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-top: 10px;
        }
        
        /* FAQ */
        .faq-item {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            margin-bottom: 20px;
            overflow: hidden;
        }
        
        .faq-question {
            padding: 25px;
            cursor: pointer;
            font-weight: 600;
            font-size: 18px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: all 0.3s ease;
        }
        
        .faq-question:hover {
            background: rgba(255, 255, 255, 0.1);
        }
        
        .faq-answer {
            padding: 0 25px 25px;
            color: #d0d0d0;
            line-height: 1.6;
        }
        
        /* Responsive Design */
        @media (max-width: 1024px) {
            .container {
                padding: 0 30px;
            }
            
            .section {
                padding: 80px 0;
            }
        }
        
        @media (max-width: 768px) {
            .container {
                padding: 0 20px;
            }
            
            .hero {
                padding: 80px 0;
            }
            
            .section {
                padding: 60px 0;
            }
            
            .problem-grid,
            .stats-grid {
                grid-template-columns: 1fr;
            }
            
            .vsl-icon {
                width: 80px;
                height: 80px;
            }
            
            .vsl-icon::before {
                font-size: 30px;
            }
            
            .cta-primary {
                padding: 15px 30px;
                font-size: 18px;
            }
        }
        
        /* Scroll animations */
        .fade-in-up {
            opacity: 0;
            transform: translateY(50px);
            transition: all 0.8s ease;
        }
        
        .fade-in-up.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <div class="bg-animation">
        <div class="bg-gradient"></div>
    </div>

    <!-- HERO SECTION -->
    <section class="hero">
        <div class="container">
            <div class="preheader">FOR YOUTUBE CREATORS STUCK UNDER 10K SUBSCRIBERS</div>
            
            <h1>Scale Your YouTube Channel to <span class="highlight">100K+ Subscribers</span> and Go Full-Time in 12 Months</h1>
            
            <div class="subheader">
                Without years of trial-and-error, algorithm confusion, or burning out from inconsistent content creation
            </div>
            
            <div class="vsl-container">
                <a href="https://docs.google.com/document/d/1UIrJC20SgqaKMBiWeyqz1BkJkFhoNFpcixPiBWx7qN8/edit?usp=sharing" class="vsl-icon" target="_blank"></a>
                <div class="vsl-text">Click Here To See The: VSL I WROTE FOR YOU</div>
            </div>
            
            <div style="text-align: center;">
                <a href="#offer" class="cta-primary">Book Your Strategy Call Now</a>
            </div>
        </div>
    </section>

    <!-- PROBLEM IDENTIFICATION -->
    <section class="section fade-in-up">
        <div class="container">
            <h2>You're Trapped in the YouTube Struggle Cycle...</h2>
            
            <div class="section-content">
                <p><strong>You pour your heart into every video.</strong></p>
                
                <p>You research trending topics... spend hours editing... craft the perfect thumbnail... hit publish...</p>
                
                <p>And then... <em>crickets.</em></p>
                
                <p>Maybe you get 47 views. Maybe 200 if you're lucky.</p>
                
                <div class="problem-grid">
                    <div class="problem-card">
                        <div class="problem-icon">😤</div>
                        <h3>Algorithm Frustration</h3>
                        <p>You've tried every "YouTube hack" online. Nothing works consistently. The algorithm feels like a black box designed to crush small creators.</p>
                    </div>
                    
                    <div class="problem-card">
                        <div class="problem-icon">💸</div>
                        <h3>Zero Monetization</h3>
                        <p>Your channel makes $0 despite months of effort. You watch other creators with worse content somehow landing sponsorships while you're invisible.</p>
                    </div>
                    
                    <div class="problem-card">
                        <div class="problem-icon">🔥</div>
                        <h3>Creator Burnout</h3>
                        <p>You're exhausted from constantly creating without results. Family and friends are starting to question if this "YouTube thing" is just a waste of time.</p>
                    </div>
                </div>
                
                <p><strong>Here's what keeps you up at night:</strong></p>
                
                <p>"What if I'm just not cut out for this?"</p>
                
                <p>"What if I waste another year creating videos that nobody watches?"</p>
                
                <p>"What if I never break through and have to give up on my dream?"</p>
                
                <p>You've tried everything... YouTube courses that teach outdated tactics... generic advice about "posting consistently"... expensive tools that promise instant growth...</p>
                
                <p><strong>But nothing addresses the real problem:</strong></p>
                
                <p class="highlight-text">Most creators are building their channel backwards. They focus on views instead of systems. Tactics instead of strategy. And content instead of business.</p>
                
                <p>There's a better way. A <em>proven</em> way that's helped thousands of creators break through their growth ceiling...</p>
            </div>
        </div>
    </section>

    <!-- ORIGIN STORY -->
    <section class="section fade-in-up">
        <div class="container">
            <h2>How I Cracked the Code After Watching 1,000+ Channels Fail</h2>
            
            <div class="section-content">
                <p>Three years ago, I was exactly where you are.</p>
                
                <p>I had all the "right" advice. I knew about thumbnails, titles, and trending topics. I understood basic SEO.</p>
                
                <p><strong>But I was stuck at 2,847 subscribers.</strong></p>
                
                <p>Sound familiar?</p>
                
                <p>I'd spend 20+ hours per week creating content... only to watch channels with half my effort blow past me.</p>
                
                <p>That's when I got obsessed with one question:</p>
                
                <p class="highlight-text">"What do the channels that actually break through do differently?"</p>
                
                <p>I spent the next 18 months analyzing over 1,000 YouTube channels across every niche imaginable.</p>
                
                <p>I studied their content patterns... their audience behavior... their monetization strategies...</p>
                
                <p><strong>And I found something shocking:</strong></p>
                
                <p>The creators who scale to 100K+ and beyond don't just make good content. They build <em>systems</em>.</p>
                
                <p>They don't chase algorithm hacks. They identify their unique "spark" - the specific angle that makes their audience obsessed - and systematically amplify it.</p>
                
                <p>They don't just create videos. They build content machines designed to turn viewers into loyal subscribers, customers, and fans.</p>
                
                <p><strong>Here's why most YouTube advice fails:</strong></p>
                
                <p>It treats all creators the same. But a gaming channel scales differently than a business channel. A tutorial channel has different needs than an entertainment channel.</p>
                
                <p>Generic advice = generic results.</p>
                
                <p>Once I understood this, everything changed. I developed a stage-specific system that addresses exactly where YOU are right now... and maps out the exact path to where you want to be.</p>
            </div>
        </div>
    </section>

    <!-- SOLUTION REVELATION -->
    <section class="section fade-in-up">
        <div class="container">
            <h2>The RadicalYT Growth System That Changes Everything</h2>
            
            <div class="section-content">
                <p>Here's what I discovered after working with over 2,000 YouTube creators:</p>
                
                <p><strong>Every successful channel follows the same growth pattern.</strong></p>
                
                <p>There are predictable stages: 0→1K→10K→100K→1M+</p>
                
                <p>And at each stage, you need different strategies, different content approaches, and different monetization methods.</p>
                
                <p class="highlight-text">Most creators fail because they're using 100K+ tactics when they're still at the 1K stage.</p>
                
                <div class="stats-grid">
                    <div class="stat-card">
                        <span class="stat-number">89%</span>
                        <span class="stat-label">Of creators use wrong-stage strategies</span>
                    </div>
                    
                    <div class="stat-card">
                        <span class="stat-number">73%</span>
                        <span class="stat-label">Never find their unique "spark"</span>
                    </div>
                    
                    <div class="stat-card">
                        <span class="stat-number">91%</span>
                        <span class="stat-label">Focus on views over systems</span>
                    </div>
                </div>
                
                <p><strong>The RadicalYT system fixes this by:</strong></p>
                
                <ul class="benefits-list">
                    <li><strong>Identifying Your Growth Stage:</strong> We pinpoint exactly where you are right now and what specific actions will move you to the next level → so you stop wasting time on tactics that don't work for your current position → and start seeing results within weeks, not months</li>
                    
                    <li><strong>Finding Your Unique Spark:</strong> We help you discover the specific angle, personality, or approach that makes YOU irreplaceable in your niche → so you stop competing with everyone else → and start building a loyal audience that chooses you over bigger channels</li>
                    
                    <li><strong>Building Content Systems:</strong> We create repeatable frameworks for ideation, creation, and optimization that work on autopilot → so you stop feeling overwhelmed by constant content pressure → and start producing viral-worthy videos consistently</li>
                    
                    <li><strong>Monetization Mapping:</strong> We show you exactly how to turn your growing audience into multiple income streams → so you stop creating content for free → and start building the financial freedom you deserve</li>
                    
                    <li><strong>Algorithm Mastery:</strong> We decode how YouTube's algorithm actually works at your specific subscriber level → so you stop chasing random "hacks" → and start getting your content recommended to the right people automatically</li>
                </ul>
                
                <p><strong>The result?</strong></p>
                
                <p>Instead of wondering if your next video will flop... you'll have confidence knowing your system works.</p>
                
                <p>Instead of burning out from endless content creation... you'll have streamlined processes that save you 15+ hours per week.</p>
                
                <p>Instead of making $0 from your passion... you'll have multiple revenue streams flowing from your channel.</p>
            </div>
        </div>
    </section>

    <!-- PRODUCT INTRODUCTION -->
    <section class="section fade-in-up">
        <div class="container">
            <h2>Introducing RadicalYT: Your Personal YouTube Growth Consulting</h2>
            
            <div class="section-content">
                <p>This isn't another generic course or cookie-cutter program.</p>
                
                <p><strong>RadicalYT is 1:1 strategic consulting designed specifically for YOUR channel, YOUR niche, and YOUR growth stage.</strong></p>
                
                <p>Here's exactly what you get:</p>
                
                <ul class="benefits-list">
                    <li><strong>Personal Growth Assessment:</strong> Deep dive analysis of your current channel, identifying hidden growth blockers and untapped opportunities most creators never see → so you finally understand why you're stuck → and get a clear roadmap out</li>
                    
                    <li><strong>Stage-Specific Strategy:</strong> Custom content and growth plan based on proven patterns from your subscriber level → so you stop using advanced tactics too early → and start implementing strategies that actually work for where you are right now</li>
                    
                    <li><strong>Spark Discovery Session:</strong> Uncover your unique content angle that makes you irreplaceable in your niche → so you stop blending in with everyone else → and start attracting viewers who become obsessed with YOUR specific approach</li>
                    
                    <li><strong>Content System Implementation:</strong> Proven templates and frameworks for ideation, creation, and optimization → so you stop staring at blank screens wondering what to create → and start pumping out engaging content systematically</li>
                    
                    <li><strong>Monetization Blueprint:</strong> Revenue strategy tailored to your audience and growth level → so you stop creating content for free → and start building income streams that let you quit your day job</li>
                    
                    <li><strong>Algorithm Optimization:</strong> Platform-specific tactics for getting your content discovered and recommended → so you stop relying on luck → and start getting consistent organic reach</li>
                </ul>
                
                <p><strong>Why this works when everything else fails:</strong></p>
                
                <p>Most YouTube advice is one-size-fits-all. But a tech reviewer needs different strategies than a lifestyle vlogger. A tutorial creator has different monetization opportunities than an entertainment channel.</p>
                
                <p>RadicalYT recognizes this. Every strategy is personalized to YOUR unique situation.</p>
                
                <p>Plus, you're not learning alone. You have direct access to someone who's guided hundreds of creators through this exact journey.</p>
                
                <p><strong>Compare this to what you've tried before:</strong></p>
                
                <p>❌ Generic YouTube courses → RadicalYT gives you personalized strategy</p>
                <p>❌ Random "algorithm hacks" → RadicalYT teaches proven systems</p>
                <p>❌ Learning alone → RadicalYT provides ongoing expert guidance</p>
                <p>❌ Hoping for the best → RadicalYT guarantees a clear path forward</p>
            </div>
        </div>
    </section>

    <!-- OFFER STRUCTURE -->
    <section class="section fade-in-up" id="offer">
        <div class="container">
            <h2>How to Get Started With RadicalYT Today</h2>
            
            <div class="section-content">
                <p><strong>Here's how RadicalYT consulting works:</strong></p>
                
                <p>Step 1: You book a strategy call using the button below</p>
                <p>Step 2: We analyze your channel and current situation</p>
                <p>Step 3: I show you exactly what's holding you back and how to fix it</p>
                <p>Step 4: We map out your personalized growth plan</p>
                <p>Step 5: You start implementing with my ongoing guidance</p>
                
                <p><strong>This isn't for everyone.</strong></p>
                
                <p>RadicalYT consulting is only for creators who:</p>
                
                <ul class="benefits-list">
                    <li>Are serious about turning their channel into a real business</li>
                    <li>Want to work with proven systems, not chase random hacks</li>
                    <li>Are ready to invest in professional guidance to accelerate their results</li>
                    <li>Understand that sustainable growth takes strategic implementation</li>
                </ul>
                
                <p><strong>If that sounds like you...</strong></p>
                
                <p>The first step is booking a strategy call where we'll:</p>
                
                <p>• Analyze your current channel and growth blockers</p>
                <p>• Identify your unique positioning opportunity</p>
                <p>• Map out your path to 100K+ subscribers</p>
                <p>• Discuss how RadicalYT consulting can accelerate your results</p>
                
                <div style="text-align: center; margin: 50px 0;">
                    <a href="#" class="cta-primary">Book Your Free Strategy Call Now</a>
                </div>
                
                <p><strong>Fair Warning:</strong> I only take on 10 new clients per month. Once those spots are filled, you'll have to wait until next month.</p>
                
                <p>Don't let another month pass wondering "what if."</p>
                
                <p>Book your call now and let's build the YouTube channel that changes your life.</p>
            </div>
        </div>
    </section>

    <!-- FAQ SECTION -->
    <section class="section fade-in-up">
        <div class="container">
            <h2>Questions? I've Got Answers.</h2>
            
            <div class="section-content">
                <div class="faq-item">
                    <div class="faq-question">
                        Will this work for my specific niche?
                        <span>+</span>
                    </div>
                    <div class="faq-answer">
                        RadicalYT has worked for creators in over 50 different niches - from gaming and tech to cooking and business. The principles are universal, but the application is always customized to your specific audience and content style. During our strategy call, I'll show you exactly how these systems apply to YOUR niche.
                    </div>
                </div>
                
                <div class="faq-item">
                    <div class="faq-question">
                        I'm too small - should I wait until I'm bigger?
                        <span>+</span>
                    </div>
                    <div class="faq-answer">
                        This is exactly backwards thinking. The earlier you implement proper systems, the faster you'll grow. I've helped creators go from 200 subscribers to 50K+ in under a year. Starting with the right strategy is what separates creators who scale from those who stay stuck. Your size now doesn't matter - your growth trajectory does.
                    </div>
                </div>
                
                <div class="faq-item">
                    <div class="faq-question">
                        What if I don't have time for complex systems?
                        <span>+</span>
                    </div>
                    <div class="faq-answer">
                        RadicalYT systems are designed to SAVE you time, not cost you time. Most creators waste 15-20 hours per week on ineffective activities. Our streamlined approach typically saves clients 10+ hours weekly while producing better results. If you're too busy to implement proper systems, you're too busy to succeed on YouTube.
                    </div>
                </div>
                
                <div class="faq-item">
                    <div class="faq-question">
                        How is this different from other YouTube courses?
                        <span>+</span>
                    </div>
                    <div class="faq-answer">
                        Most courses teach generic tactics that might work for some creators. RadicalYT is 1:1 consulting that creates a custom strategy for YOUR specific situation, niche, and goals. You're not getting pre-recorded videos - you're getting personalized guidance from someone who's analyzed over 2,000 successful channels. It's the difference between following a map and having a personal guide.
                    </div>
                </div>
                
                <div class="faq-item">
                    <div class="faq-question">
                        What if YouTube changes its algorithm?
                        <span>+</span>
                    </div>
                    <div class="faq-answer">
                        Algorithm changes happen, but the core principles of audience psychology and content strategy remain constant. RadicalYT focuses on building sustainable systems that work regardless of platform changes. When YouTube tweaks something, we adapt quickly - but your foundation stays solid.
                    </div>
                </div>
                
                <div style="text-align: center; margin: 50px 0;">
                    <a href="#" class="cta-primary">Stop Spinning Your Wheels - Book Your Call Now</a>
                </div>
                
                <p style="text-align: center; color: #b0b0b0; font-style: italic;">
                    Your dream YouTube channel is one strategy call away. Don't let another month pass watching others succeed while you stay stuck.
                </p>
            </div>
        </div>
    </section>

    <script>
        // Smooth scrolling for CTA buttons
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Scroll animations
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

        document.querySelectorAll('.fade-in-up').forEach(el => {
            observer.observe(el);
        });

        // FAQ Toggle Functionality
        document.querySelectorAll('.faq-question').forEach(question => {
            question.addEventListener('click', () => {
                const answer = question.nextElementSibling;
                const icon = question.querySelector('span');
                
                if (answer.style.display === 'block') {
                    answer.style.display = 'none';
                    icon.textContent = '+';
                } else {
                    // Close all other FAQs
                    document.querySelectorAll('.faq-answer').forEach(a => a.style.display = 'none');
                    document.querySelectorAll('.faq-question span').forEach(i => i.textContent = '+');
                    
                    // Open this FAQ
                    answer.style.display = 'block';
                    icon.textContent = '−';
                }
            });
        });

        // Parallax effect for background
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const parallax = document.querySelector('.bg-gradient');
            const speed = scrolled * 0.5;
            parallax.style.transform = `translate(-50%, -50%) translateY(${speed}px) rotate(${scrolled * 0.05}deg)`;
        });

        // Add glowing effect on hover for cards
        document.querySelectorAll('.problem-card, .stat-card, .benefits-list li').forEach(card => {
            card.addEventListener('mouseenter', () => {
                card.style.boxShadow = '0 20px 60px rgba(255, 0, 87, 0.2)';
            });
            
            card.addEventListener('mouseleave', () => {
                card.style.boxShadow = '';
            });
        });

        // Dynamic typing effect for hero text (optional enhancement)
        function typeWriter(element, text, speed = 50) {
            let i = 0;
            element.innerHTML = '';
            
            function type() {
                if (i < text.length) {
                    element.innerHTML += text.charAt(i);
                    i++;
                    setTimeout(type, speed);
                }
            }
            type();
        }

        // Intersection Observer for counter animation
        function animateCounters() {
            const counters = document.querySelectorAll('.stat-number');
            
            counters.forEach(counter => {
                const target = parseInt(counter.textContent);
                let count = 0;
                const increment = target / 100;
                
                const timer = setInterval(() => {
                    count += increment;
                    if (count >= target) {
                        counter.textContent = target + '%';
                        clearInterval(timer);
                    } else {
                        counter.textContent = Math.floor(count) + '%';
                    }
                }, 20);
            });
        }

        // Trigger counter animation when stats section is visible
        const statsObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    animateCounters();
                    statsObserver.unobserve(entry.target);
                }
            });
        });

        const statsSection = document.querySelector('.stats-grid');
        if (statsSection) {
            statsObserver.observe(statsSection);
        }

        // Add some interactive sparkle effects
        function createSparkle() {
            const sparkle = document.createElement('div');
            sparkle.className = 'sparkle';
            sparkle.style.cssText = `
                position: fixed;
                width: 4px;
                height: 4px;
                background: linear-gradient(45deg, #ff0057, #0095ff);
                border-radius: 50%;
                pointer-events: none;
                z-index: 1000;
                animation: sparkleFloat 2s ease-out forwards;
            `;
            
            const style = document.createElement('style');
            style.textContent = `
                @keyframes sparkleFloat {
                    0% {
                        opacity: 1;
                        transform: translateY(0) scale(0);
                    }
                    50% {
                        opacity: 1;
                        transform: translateY(-100px) scale(1);
                    }
                    100% {
                        opacity: 0;
                        transform: translateY(-200px) scale(0);
                    }
                }
            `;
            document.head.appendChild(style);
            
            sparkle.style.left = Math.random() * window.innerWidth + 'px';
            sparkle.style.top = window.innerHeight + 'px';
            
            document.body.appendChild(sparkle);
            
            setTimeout(() => {
                sparkle.remove();
            }, 2000);
        }

        // Create sparkles periodically
        setInterval(createSparkle, 3000);
    </script>
