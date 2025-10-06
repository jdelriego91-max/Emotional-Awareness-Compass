<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Module 1: Your Emotional Compass</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=Crimson+Pro:wght@400;600&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: linear-gradient(135deg, #0d1b24 0%, #1e3f4d 100%);
            color: #e8e8e8;
            padding: 20px;
            line-height: 1.7;
        }
        
        .container {
            max-width: 900px;
            margin: 0 auto;
        }
        
        .header {
            text-align: center;
            margin-bottom: 40px;
        }
        
        .module-badge {
            display: inline-block;
            background: #c55339;
            color: #fff;
            padding: 10px 28px;
            border-radius: 30px;
            font-size: 13px;
            font-weight: 700;
            letter-spacing: 1px;
            margin-bottom: 20px;
            text-transform: uppercase;
            box-shadow: 0 4px 15px rgba(197, 83, 57, 0.3);
        }
        
        h1 {
            font-family: 'Crimson Pro', serif;
            font-size: 2.8rem;
            color: #d4a5a5;
            margin-bottom: 15px;
            font-weight: 600;
        }
        
        .subtitle {
            color: #a89090;
            font-size: 1.15rem;
            font-weight: 400;
        }
        
        .progress-container {
            margin-bottom: 35px;
        }
        
        .progress-info {
            display: flex;
            justify-content: space-between;
            font-size: 13px;
            color: #a89090;
            margin-bottom: 10px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }
        
        .progress-bar {
            height: 8px;
            background: rgba(98, 54, 67, 0.4);
            border-radius: 10px;
            overflow: hidden;
        }
        
        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, #c55339 0%, #a85d75 100%);
            transition: width 0.6s cubic-bezier(0.4, 0, 0.2, 1);
            box-shadow: 0 0 10px rgba(197, 83, 57, 0.5);
        }
        
        .content-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(212, 165, 165, 0.1);
            border-radius: 16px;
            padding: 45px;
            margin-bottom: 25px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
        }
        
        h2 {
            font-family: 'Crimson Pro', serif;
            font-size: 2.2rem;
            color: #d4a5a5;
            margin-bottom: 30px;
            font-weight: 600;
        }
        
        h3 {
            font-family: 'Crimson Pro', serif;
            font-size: 1.6rem;
            color: #d4a5a5;
            margin-bottom: 15px;
            font-weight: 600;
        }
        
        h4 {
            font-size: 1.2rem;
            color: #d4a5a5;
            margin-bottom: 12px;
            font-weight: 700;
        }
        
        p {
            font-size: 1.05rem;
            line-height: 1.8;
            color: #c9c9c9;
        }
        
        .slide {
            display: none;
        }
        
        .slide.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }
        
        @keyframes fadeIn {
            from { 
                opacity: 0; 
                transform: translateY(15px); 
            }
            to { 
                opacity: 1; 
                transform: translateY(0); 
            }
        }
        
        .callout {
            padding: 25px;
            border-radius: 10px;
            margin: 25px 0;
            border-left: 5px solid;
            background: rgba(255, 255, 255, 0.03);
        }
        
        .callout-primary {
            border-color: #c55339;
            background: rgba(197, 83, 57, 0.08);
        }
        
        .callout-secondary {
            border-color: #a85d75;
            background: rgba(168, 93, 117, 0.08);
        }
        
        .callout-tertiary {
            border-color: #623643;
            background: rgba(98, 54, 67, 0.08);
        }
        
        .callout-highlight {
            border-color: #d4a5a5;
            background: rgba(212, 165, 165, 0.08);
        }
        
        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 25px;
            margin: 35px 0;
        }
        
        .card {
            background: rgba(255, 255, 255, 0.05);
            padding: 30px;
            border-radius: 12px;
            border-top: 4px solid;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
        }
        
        .card-primary { border-color: #c55339; }
        .card-secondary { border-color: #a85d75; }
        .card-tertiary { border-color: #623643; }
        
        .card-icon {
            width: 48px;
            height: 48px;
            margin-bottom: 15px;
            opacity: 0.9;
        }
        
        .scenario-card {
            border: 2px solid rgba(212, 165, 165, 0.2);
            background: rgba(255, 255, 255, 0.03);
            padding: 30px;
            border-radius: 12px;
            margin: 25px 0;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .scenario-card:hover {
            border-color: rgba(212, 165, 165, 0.4);
            background: rgba(255, 255, 255, 0.05);
        }
        
        .scenario-card.selected {
            border-color: #c55339;
            background: rgba(197, 83, 57, 0.1);
            box-shadow: 0 0 20px rgba(197, 83, 57, 0.2);
        }
        
        .scenario-details {
            display: none;
            margin-top: 25px;
            padding-top: 25px;
            border-top: 2px solid rgba(197, 83, 57, 0.3);
        }
        
        .scenario-card.selected .scenario-details {
            display: block;
            animation: fadeIn 0.4s ease;
        }
        
        .reveal-btn {
            color: #c55339;
            font-weight: 600;
            margin-top: 15px;
            display: inline-flex;
            align-items: center;
            font-size: 0.95rem;
            letter-spacing: 0.3px;
        }
        
        .scenario-card.selected .reveal-btn {
            display: none;
        }
        
        .detail-item {
            margin: 18px 0;
            padding-left: 15px;
        }
        
        .detail-label {
            font-weight: 700;
            color: #c55339;
            margin-right: 8px;
        }
        
        .detail-highlight {
            background: rgba(255, 255, 255, 0.05);
            padding: 20px;
            border-radius: 10px;
            border-left: 4px solid #c55339;
            margin-top: 20px;
        }
        
        .input-group {
            background: rgba(255, 255, 255, 0.05);
            padding: 28px;
            border-radius: 12px;
            border: 1px solid rgba(212, 165, 165, 0.15);
            margin: 25px 0;
            transition: border-color 0.3s ease;
        }
        
        .input-group:focus-within {
            border-color: rgba(197, 83, 57, 0.5);
        }
        
        .input-group label {
            display: flex;
            align-items: center;
            font-weight: 700;
            color: #d4a5a5;
            margin-bottom: 15px;
            font-size: 1.1rem;
        }
        
        .color-indicator {
            width: 10px;
            height: 10px;
            border-radius: 50%;
            margin-right: 12px;
            flex-shrink: 0;
        }
        
        .indicator-primary { background: #c55339; box-shadow: 0 0 8px rgba(197, 83, 57, 0.5); }
        .indicator-secondary { background: #a85d75; box-shadow: 0 0 8px rgba(168, 93, 117, 0.5); }
        .indicator-tertiary { background: #623643; box-shadow: 0 0 8px rgba(98, 54, 67, 0.5); }
        
        input[type="text"] {
            width: 100%;
            padding: 14px;
            border: 2px solid rgba(212, 165, 165, 0.2);
            border-radius: 8px;
            font-size: 1rem;
            background: rgba(255, 255, 255, 0.05);
            color: #e8e8e8;
            transition: all 0.3s ease;
            font-family: 'Inter', sans-serif;
        }
        
        input[type="text"]:focus {
            outline: none;
            border-color: #c55339;
            background: rgba(255, 255, 255, 0.08);
            box-shadow: 0 0 15px rgba(197, 83, 57, 0.2);
        }
        
        input[type="text"]::placeholder {
            color: #888;
        }
        
        .example-text {
            font-size: 0.9rem;
            color: #a89090;
            font-style: italic;
            margin-top: 10px;
        }
        
        .checklist {
            list-style: none;
            padding: 0;
        }
        
        .checklist li {
            display: flex;
            align-items: start;
            margin: 20px 0;
            padding: 15px;
            background: rgba(255, 255, 255, 0.03);
            border-radius: 8px;
            border-left: 3px solid rgba(197, 83, 57, 0.5);
        }
        
        .check-mark {
            color: #c55339;
            font-weight: 700;
            margin-right: 15px;
            font-size: 1.2rem;
            flex-shrink: 0;
        }
        
        button {
            padding: 16px 32px;
            border-radius: 10px;
            font-weight: 700;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            border: none;
            font-family: 'Inter', sans-serif;
            letter-spacing: 0.3px;
        }
        
        .btn-primary {
            background: linear-gradient(135deg, #c55339 0%, #a85d75 100%);
            color: #fff;
            box-shadow: 0 4px 15px rgba(197, 83, 57, 0.3);
        }
        
        .btn-primary:hover:not(:disabled) {
            background: linear-gradient(135deg, #d66347 0%, #b96d85 100%);
            box-shadow: 0 6px 20px rgba(197, 83, 57, 0.4);
            transform: translateY(-2px);
        }
        
        .btn-secondary {
            background: rgba(98, 54, 67, 0.6);
            color: #fff;
            border: 1px solid rgba(212, 165, 165, 0.3);
        }
        
        .btn-secondary:hover:not(:disabled) {
            background: rgba(98, 54, 67, 0.8);
            border-color: rgba(212, 165, 165, 0.5);
            transform: translateY(-2px);
        }
        
        button:disabled {
            background: rgba(98, 54, 67, 0.3);
            color: #888;
            cursor: not-allowed;
            box-shadow: none;
        }
        
        .navigation {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 30px;
        }
        
        .dots {
            display: flex;
            gap: 10px;
        }
        
        .dot {
            width: 10px;
            height: 10px;
            border-radius: 50%;
            background: rgba(212, 165, 165, 0.3);
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .dot:hover {
            background: rgba(212, 165, 165, 0.5);
            transform: scale(1.2);
        }
        
        .dot.active {
            width: 28px;
            background: #c55339;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(197, 83, 57, 0.5);
        }
        
        .results-box {
            background: rgba(197, 83, 57, 0.1);
            border: 2px solid #c55339;
            border-radius: 12px;
            padding: 30px;
            margin-top: 30px;
            display: none;
            box-shadow: 0 0 25px rgba(197, 83, 57, 0.2);
        }
        
        .results-box.show {
            display: block;
            animation: fadeIn 0.5s ease;
        }
        
        .state-display {
            background: rgba(255, 255, 255, 0.05);
            padding: 25px;
            border-radius: 10px;
            border-left: 4px solid #c55339;
            margin: 20px 0;
        }
        
        .state-display p {
            margin: 12px 0;
        }
        
        .gradient-header {
            background: linear-gradient(135deg, #c55339 0%, #623643 100%);
            color: #fff;
            padding: 35px;
            border-radius: 12px;
            box-shadow: 0 8px 25px rgba(197, 83, 57, 0.3);
        }
        
        .without-box {
            background: rgba(98, 54, 67, 0.2);
            padding: 25px;
            border-radius: 10px;
            border-left: 4px solid rgba(168, 93, 117, 0.6);
            margin: 25px 0;
        }
        
        .with-box {
            background: rgba(197, 83, 57, 0.15);
            padding: 25px;
            border-radius: 10px;
            border-left: 4px solid #c55339;
            margin: 25px 0;
        }
        
        .closing-statement {
            text-align: center;
            padding: 40px;
            background: rgba(255, 255, 255, 0.03);
            border-radius: 12px;
            margin-top: 30px;
            border: 1px solid rgba(212, 165, 165, 0.2);
        }
        
        strong {
            color: #d4a5a5;
            font-weight: 700;
        }
        
        @media (max-width: 768px) {
            body {
                padding: 15px;
            }
            
            .content-card {
                padding: 30px 25px;
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
            
            .grid-3 {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div class="module-badge">Module 1: Self-Awareness</div>
            <h1>Your Emotional Compass</h1>
            <p class="subtitle">The Foundation for Protecting Your Growth</p>
        </div>

        <div class="progress-container">
            <div class="progress-info">
                <span>Progress</span>
                <span><span id="current-slide">1</span> of <span id="total-slides">6</span></span>
            </div>
            <div class="progress-bar">
                <div class="progress-fill" id="progress-fill"></div>
            </div>
        </div>

        <div class="content-card">
            <!-- Slide 1: Welcome -->
            <div class="slide active" data-slide="0">
                <h2>Welcome Back, Warrior</h2>
                <div class="callout callout-primary">
                    <p>
                        You've been on the mountain. You've done the hard work. You've looked inward and declared who you are becoming.
                    </p>
                </div>
                
                <p style="margin: 30px 0;">
                    Now you're home. And here's the truth: <strong>the retreat changed you, but the real battle is keeping that growth alive.</strong>
                </p>
                
                <p style="margin: 30px 0;">
                    Think of what you discovered about yourself at the retreat like a precious plant you brought back from the mountain. It's alive. It's real. But it needs care, attention, and the right conditions to grow.
                </p>
                
                <div class="callout callout-secondary">
                    <p style="font-weight: 600;">
                        The first step in protecting your growth? Knowing exactly where you are right now.
                    </p>
                </div>
                
                <p style="color: #a89090; font-style: italic; margin-top: 25px;">
                    This is your emotional compass. Let's learn to read it.
                </p>
            </div>

            <!-- Slide 2: Concept -->
            <div class="slide" data-slide="1">
                <h2>What Is Self-Awareness?</h2>
                <div class="callout callout-highlight">
                    <h3 style="margin-bottom: 20px;">Self-awareness is simply this:</h3>
                    <p style="font-size: 1.15rem;">
                        Knowing what you're feeling, why you're feeling it, and how it's affecting you right now.
                    </p>
                </div>

                <p style="margin: 30px 0;">
                    It's like having a dashboard in your car. The check engine light comes on—that's information. You don't ignore it. You don't punch the dashboard. You check what's happening under the hood.
                </p>

                <div class="grid-3">
                    <div class="card card-primary">
                        <svg class="card-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"></path>
                        </svg>
                        <h4>What you're feeling</h4>
                        <p style="color: #b0b0b0;">The emotion itself: anger, sadness, joy, anxiety</p>
                    </div>
                    
                    <div class="card card-secondary">
                        <svg class="card-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"></path>
                        </svg>
                        <h4>Why you're feeling it</h4>
                        <p style="color: #b0b0b0;">The trigger: what just happened or what you're thinking about</p>
                    </div>
                    
                    <div class="card card-tertiary">
                        <svg class="card-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path>
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path>
                        </svg>
                        <h4>How it's affecting you</h4>
                        <p style="color: #b0b0b0;">Your body, thoughts, and actions right now</p>
                    </div>
                </div>

                <div class="callout callout-primary">
                    <p>
                        <strong>For warriors returning from the retreat:</strong> You've already started this work. You've named your struggles. You've identified your wolves. Now we're going deeper—learning to catch these moments in real-time, every single day.
                    </p>
                </div>
            </div>

            <!-- Slide 3: Example -->
            <div class="slide" data-slide="2">
                <h2>Real Example: Morning Coffee</h2>
                <p style="margin-bottom: 30px;">
                    Let's say you're having coffee, and someone asks: <strong>"So, how was that retreat you went to?"</strong>
                </p>

                <div class="without-box">
                    <h4 style="margin-bottom: 15px;">WITHOUT Self-Awareness:</h4>
                    <p style="margin-bottom: 12px;">You feel your chest tighten. You give a quick answer: "It was fine." You change the subject. Maybe you get irritated. You're not sure why.</p>
                    <p style="color: #a89090; font-style: italic;">You just reacted. You missed valuable information.</p>
                </div>

                <div class="with-box">
                    <h4 style="margin-bottom: 20px;">WITH Self-Awareness:</h4>
                    <div class="detail-item">
                        <span class="detail-label">What you notice:</span>
                        <span>Chest tightening, sudden defensiveness</span>
                    </div>
                    <div class="detail-item">
                        <span class="detail-label">The emotion:</span>
                        <span>Fear mixed with protectiveness</span>
                    </div>
                    <div class="detail-item">
                        <span class="detail-label">The trigger:</span>
                        <span>Someone asking about something deeply personal—that precious plant you're protecting</span>
                    </div>
                    <div class="detail-item">
                        <span class="detail-label">The why:</span>
                        <span>You're worried they won't understand. You're not ready to share it casually. That experience is sacred to you.</span>
                    </div>
                    <div class="detail-item">
                        <span class="detail-label">Your choice:</span>
                        <span>"It was powerful. I'm still processing it." Then you decide if you want to say more.</span>
                    </div>
                </div>

                <div class="callout callout-primary" style="margin-top: 30px;">
                    <p style="font-weight: 600; margin-bottom: 12px;">See the difference?</p>
                    <p>
                        Same moment. Same person. But with self-awareness, you're <strong>in the driver's seat</strong> instead of being driven by emotions you don't understand.
                    </p>
                </div>
            </div>

            <!-- Slide 4: Interactive -->
            <div class="slide" data-slide="3">
                <h2>Try It: Emotion Spotting</h2>
                <p style="margin-bottom: 30px;">
                    Let's practice recognizing emotions and their effects. Read each scenario and click to see what's really happening:
                </p>

                <div class="scenario-card" onclick="toggleScenario(0)">
                    <p style="font-weight: 600; margin-bottom: 15px; font-size: 1.1rem;">
                        Scenario 1: You're scrolling social media and see photos of your old team at work. Your jaw clenches. You close the app.
                    </p>
                    <div class="reveal-btn">
                        Click to see what's really happening →
                    </div>
                    <div class="scenario-details">
                        <div class="detail-item">
                            <span class="detail-label">Emotion:</span>
                            <span>Grief/Loss</span>
                        </div>
                        <div class="detail-item">
                            <span class="detail-label">Trigger:</span>
                            <span>Reminder of what you're no longer part of</span>
                        </div>
                        <div class="detail-item">
                            <span class="detail-label">Effect:</span>
                            <span>Physical tension, avoidance behavior</span>
                        </div>
                        <div class="detail-highlight">
                            <span style="font-weight: 700;">Why This Matters: </span>
                            <span>You're protecting yourself from pain, but you're also cutting yourself off from feelings that need acknowledgment.</span>
                        </div>
                    </div>
                </div>

                <div class="scenario-card" onclick="toggleScenario(1)">
                    <p style="font-weight: 600; margin-bottom: 15px; font-size: 1.1rem;">
                        Scenario 2: Your spouse asks 'Are you okay?' for the third time today. You snap: 'I'm FINE.'
                    </p>
                    <div class="reveal-btn">
                        Click to see what's really happening →
                    </div>
                    <div class="scenario-details">
                        <div class="detail-item">
                            <span class="detail-label">Emotion:</span>
                            <span>Frustration/Feeling Misunderstood</span>
                        </div>
                        <div class="detail-item">
                            <span class="detail-label">Trigger:</span>
                            <span>Repeated questioning feels like doubt in your ability to handle things</span>
                        </div>
                        <div class="detail-item">
                            <span class="detail-label">Effect:</span>
                            <span>Sharp tone, pushing away support</span>
                        </div>
                        <div class="detail-highlight">
                            <span style="font-weight: 700;">Why This Matters: </span>
                            <span>The question threatens your identity as someone who's 'got it together'—something you're working hard to maintain.</span>
                        </div>
                    </div>
                </div>

                <div class="scenario-card" onclick="toggleScenario(2)">
                    <p style="font-weight: 600; margin-bottom: 15px; font-size: 1.1rem;">
                        Scenario 3: You volunteer to help a neighbor move furniture. Afterward, you feel energized instead of tired.
                    </p>
                    <div class="reveal-btn">
                        Click to see what's really happening →
                    </div>
                    <div class="scenario-details">
                        <div class="detail-item">
                            <span class="detail-label">Emotion:</span>
                            <span>Purpose/Meaning</span>
                        </div>
                        <div class="detail-item">
                            <span class="detail-label">Trigger:</span>
                            <span>Acting in service to others</span>
                        </div>
                        <div class="detail-item">
                            <span class="detail-label">Effect:</span>
                            <span>Increased energy, positive mood</span>
                        </div>
                        <div class="detail-highlight">
                            <span style="font-weight: 700;">Why This Matters: </span>
                            <span>This aligned with your values from the retreat—service as the hero's gift. Your body is telling you you're on the right path.</span>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Slide 5: Check-in -->
            <div class="slide" data-slide="4">
                <h2>Your Check-In: Where Are You Right Now?</h2>
                <div class="callout callout-highlight">
                    <p>
                        <strong>Remember the Hero's Journey?</strong> You left the ordinary world, faced trials, gained wisdom, and returned with a gift. But the journey isn't over. The hero must learn to live in both worlds—bringing the mountain back to the valley.
                    </p>
                </div>

                <p style="margin: 30px 0;">
                    Right now, in this moment, where are you? Let's take inventory—no judgment, just honest observation.
                </p>

                <div class="input-group">
                    <label>
                        <span class="color-indicator indicator-primary"></span>
                        Physically: What do you notice in your body right now?
                    </label>
                    <input type="text" id="physical" placeholder="Tired? Tense shoulders? Restless? Calm?">
                    <p class="example-text">Example: "Tension in my jaw, low energy, feeling heavy"</p>
                </div>

                <div class="input-group">
                    <label>
                        <span class="color-indicator indicator-secondary"></span>
                        Mentally: What's your mind doing?
                    </label>
                    <input type="text" id="mental" placeholder="Racing thoughts? Foggy? Focused? Worried about something?">
                    <p class="example-text">Example: "Thinking about tomorrow's meeting, scattered, hard to concentrate"</p>
                </div>

                <div class="input-group">
                    <label>
                        <span class="color-indicator indicator-tertiary"></span>
                        Emotionally: What are you feeling?
                    </label>
                    <input type="text" id="emotional" placeholder="Hopeful? Anxious? Proud? Overwhelmed? Mix of things?">
                    <p class="example-text">Example: "Motivated but also scared I'll lose what I gained at the retreat"</p>
                </div>

                <button class="btn-primary" style="width: 100%; padding: 18px; margin-top: 25px;" onclick="completeCheckIn()" id="checkin-btn" disabled>
                    Complete My Check-In
                </button>

                <div class="results-box" id="results-box">
                    <div>
                        <h4 style="margin-bottom: 20px; font-size: 1.4rem;">You Just Practiced Self-Awareness</h4>
                        <p style="margin-bottom: 25px;">
                            You stopped. You observed. You named what's happening. This is exactly what protects your growth.
                        </p>
                        <div class="state-display">
                            <p style="font-weight: 600; margin-bottom: 15px;">Your Current State:</p>
                            <p><strong>Physical:</strong> <span id="physical-result"></span></p>
                            <p><strong>Mental:</strong> <span id="mental-result"></span></p>
                            <p><strong>Emotional:</strong> <span id="emotional-result"></span></p>
                        </div>
                        <p style="margin-top: 25px;">
                            <strong>Remember:</strong> Awareness doesn't mean everything is perfect. It means you know where you are. And when you know where you are, you can make intentional choices about where you want to go.
                        </p>
                    </div>
                </div>
            </div>

            <!-- Slide 6: Summary -->
            <div class="slide" data-slide="5">
                <h2>Your Daily Mission</h2>
                <div class="gradient-header">
                    <h3 style="color: #fff; margin-bottom: 20px;">Self-Awareness = Protection</h3>
                    <p style="font-size: 1.1rem; color: #fff;">
                        That precious plant you brought back from the retreat? Self-awareness is how you water it, how you shield it from harsh weather, how you give it what it needs to grow.
                    </p>
                </div>

                <div class="callout callout-primary" style="margin: 30px 0;">
                    <h4 style="margin-bottom: 25px;">What You Learned Today:</h4>
                    <ul class="checklist">
                        <li>
                            <span class="check-mark">✓</span>
                            <span>Self-awareness means knowing what you're feeling, why, and how it affects you</span>
                        </li>
                        <li>
                            <span class="check-mark">✓</span>
                            <span>Every emotion carries information—it's your dashboard telling you what needs attention</span>
                        </li>
                        <li>
                            <span class="check-mark">✓</span>
                            <span>Checking in with yourself (physical, mental, emotional) keeps you grounded in reality</span>
                        </li>
                        <li>
                            <span class="check-mark">✓</span>
                            <span>Awareness gives you choice—you're driving instead of being driven</span>
                        </li>
                    </ul>
                </div>

                <div class="callout callout-secondary">
                    <h4 style="margin-bottom: 20px;">Your 24-Hour Challenge:</h4>
                    <p style="margin-bottom: 20px;">
                        Set three reminders on your phone (morning, midday, evening). When it goes off, pause for 60 seconds and ask:
                    </p>
                    <div style="background: rgba(255, 255, 255, 0.05); padding: 25px; border-radius: 10px;">
                        <p style="margin: 12px 0;"><strong>1.</strong> What am I feeling right now?</p>
                        <p style="margin: 12px 0;"><strong>2.</strong> What triggered it?</p>
                        <p style="margin: 12px 0;"><strong>3.</strong> How is it showing up in my body, thoughts, or actions?</p>
                    </div>
                    <p style="color: #a89090; font-style: italic; margin-top: 20px;">
                        Don't try to change anything. Just notice. Awareness first, always.
                    </p>
                </div>

                <div class="closing-statement">
                    <p style="font-size: 1.25rem; font-weight: 600; margin-bottom: 15px;">
                        You've returned from the mountain with a gift.
                    </p>
                    <p style="font-size: 1.1rem;">
                        Self-awareness is how you keep it alive.
                    </p>
                </div>
            </div>
        </div>

        <div class="navigation">
            <button class="btn-secondary" onclick="previousSlide()" id="prev-btn">
                ← Previous
            </button>
            
            <div class="dots" id="dots"></div>

            <button class="btn-primary" onclick="nextSlide()" id="next-btn">
                Next →
            </button>
        </div>
    </div>

    <script>
        let currentSlide = 0;
        const totalSlides = 6;

        function updateUI() {
            document.querySelectorAll('.slide').forEach(slide => {
                slide.classList.remove('active');
            });
            
            document.querySelector(`[data-slide="${currentSlide}"]`).classList.add('active');
            
            const progress = ((currentSlide + 1) / totalSlides) * 100;
            document.getElementById('progress-fill').style.width = progress + '%';
            document.getElementById('current-slide').textContent = currentSlide + 1;
            
            document.getElementById('prev-btn').disabled = currentSlide === 0;
            document.getElementById('next-btn').disabled = currentSlide === totalSlides - 1;
            
            updateDots();
        }

        function updateDots() {
            const dotsContainer = document.getElementById('dots');
            dotsContainer.innerHTML = '';
            
            for (let i = 0; i < totalSlides; i++) {
                const dot = document.createElement('div');
                dot.className = 'dot' + (i === currentSlide ? ' active' : '');
                dot.onclick = () => goToSlide(i);
                dotsContainer.appendChild(dot);
            }
        }

        function nextSlide() {
            if (currentSlide < totalSlides - 1) {
                currentSlide++;
                updateUI();
            }
        }

        function previousSlide() {
            if (currentSlide > 0) {
                currentSlide--;
                updateUI();
            }
        }

        function goToSlide(index) {
            currentSlide = index;
            updateUI();
        }

        function toggleScenario(index) {
            const cards = document.querySelectorAll('.scenario-card');
            cards[index].classList.toggle('selected');
        }

        const physicalInput = document.getElementById('physical');
        const mentalInput = document.getElementById('mental');
        const emotionalInput = document.getElementById('emotional');
        const checkinBtn = document.getElementById('checkin-btn');

        function checkInputs() {
            if (physicalInput.value && mentalInput.value && emotionalInput.value) {
                checkinBtn.disabled = false;
            } else {
                checkinBtn.disabled = true;
            }
        }

        physicalInput.addEventListener('input', checkInputs);
        mentalInput.addEventListener('input', checkInputs);
        emotionalInput.addEventListener('input', checkInputs);

        function completeCheckIn() {
            document.getElementById('physical-result').textContent = physicalInput.value;
            document.getElementById('mental-result').textContent = mentalInput.value;
            document.getElementById('emotional-result').textContent = emotionalInput.value;
            document.getElementById('results-box').classList.add('show');
        }

        updateUI();
    </script>
</body>
</html>
