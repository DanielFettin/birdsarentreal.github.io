<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Birds Aren't Real | Wake Up America</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Courier+Prime:wght@400;700&family=Oswald:wght@700&display=swap');
        
        :root {
            --navy: #1E2761;
            --crimson: #990011;
            --cream: #FCF6F5;
            --gold: #FFD700;
            --charcoal: #36454F;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Courier Prime', monospace;
            background: var(--navy);
            color: var(--cream);
            overflow-x: hidden;
            line-height: 1.6;
        }
        
        /* Animated background scanlines */
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: repeating-linear-gradient(
                0deg,
                rgba(255, 255, 255, 0.03) 0px,
                rgba(255, 255, 255, 0.03) 1px,
                transparent 1px,
                transparent 2px
            );
            pointer-events: none;
            z-index: 9999;
            animation: scanlines 8s linear infinite;
        }
        
        @keyframes scanlines {
            0% { transform: translateY(0); }
            100% { transform: translateY(10px); }
        }
        
        /* Header */
        header {
            background: var(--charcoal);
            padding: 1rem;
            border-bottom: 3px solid var(--crimson);
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 20px rgba(0,0,0,0.5);
        }
        
        .header-content {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 2rem;
            color: var(--gold);
            letter-spacing: 3px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }
        
        .classified-badge {
            background: var(--crimson);
            color: var(--cream);
            padding: 0.5rem 1rem;
            font-weight: bold;
            font-size: 0.9rem;
            transform: rotate(-2deg);
            border: 2px solid var(--cream);
            box-shadow: 3px 3px 0 rgba(0,0,0,0.3);
        }
        
        /* Hero Section */
        .hero {
            padding: 4rem 2rem;
            text-align: center;
            background: linear-gradient(135deg, var(--navy) 0%, #0a0e2e 100%);
            position: relative;
            overflow: hidden;
        }
        
        .hero::after {
            content: '👁️';
            position: absolute;
            font-size: 15rem;
            opacity: 0.05;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            animation: pulse 3s ease-in-out infinite;
        }
        
        @keyframes pulse {
            0%, 100% { opacity: 0.05; }
            50% { opacity: 0.08; }
        }
        
        .hero h1 {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 5rem;
            color: var(--cream);
            margin-bottom: 1rem;
            text-shadow: 4px 4px 8px rgba(0,0,0,0.7);
            animation: glitch 3s infinite;
            position: relative;
            z-index: 1;
        }
        
        @keyframes glitch {
            0%, 90%, 100% { transform: translate(0); }
            92% { transform: translate(-2px, 2px); }
            94% { transform: translate(2px, -2px); }
            96% { transform: translate(-2px, -2px); }
        }
        
        .hero .tagline {
            font-family: 'Oswald', sans-serif;
            font-size: 1.8rem;
            color: var(--gold);
            letter-spacing: 5px;
            margin-bottom: 2rem;
            position: relative;
            z-index: 1;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 2rem;
            color: var(--cream);
            opacity: 0.9;
            position: relative;
            z-index: 1;
        }
        
        /* Bird Counter */
        .bird-counter {
            background: rgba(255, 215, 0, 0.1);
            border: 2px solid var(--gold);
            padding: 2rem;
            margin: 3rem auto;
            max-width: 600px;
            border-radius: 10px;
            position: relative;
            z-index: 1;
        }
        
        .bird-counter h3 {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 1.5rem;
            color: var(--gold);
            margin-bottom: 1rem;
        }
        
        .counter-display {
            font-family: 'Courier Prime', monospace;
            font-size: 3rem;
            color: var(--crimson);
            font-weight: bold;
            text-shadow: 0 0 10px rgba(153, 0, 17, 0.5);
        }
        
        .counter-label {
            font-size: 0.9rem;
            color: var(--cream);
            opacity: 0.8;
            margin-top: 0.5rem;
        }
        
        /* Section Styling */
        section {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .section-title {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 3rem;
            color: var(--gold);
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
            padding-bottom: 1rem;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: var(--crimson);
        }
        
        /* Evidence Gallery */
        .evidence-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .evidence-card {
            background: var(--charcoal);
            border: 2px solid var(--crimson);
            border-radius: 8px;
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }
        
        .evidence-card:hover {
            transform: translateY(-10px) rotate(1deg);
            box-shadow: 0 10px 30px rgba(153, 0, 17, 0.5);
        }
        
        .evidence-image {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, #1E2761 0%, #0a0e2e 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 5rem;
            border-bottom: 2px solid var(--crimson);
        }
        
        .evidence-content {
            padding: 1.5rem;
        }
        
        .evidence-content h3 {
            font-family: 'Oswald', sans-serif;
            color: var(--gold);
            margin-bottom: 0.5rem;
            font-size: 1.3rem;
        }
        
        .evidence-content p {
            color: var(--cream);
            font-size: 0.95rem;
            line-height: 1.5;
        }
        
        /* Interactive Bird Detector */
        .detector {
            background: rgba(153, 0, 17, 0.1);
            border: 3px solid var(--crimson);
            padding: 3rem;
            border-radius: 10px;
            text-align: center;
            margin: 3rem auto;
            max-width: 600px;
        }
        
        .detector h3 {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 2rem;
            color: var(--crimson);
            margin-bottom: 1.5rem;
        }
        
        .detector-button {
            background: var(--crimson);
            color: var(--cream);
            border: none;
            padding: 1.5rem 3rem;
            font-family: 'Oswald', sans-serif;
            font-size: 1.3rem;
            cursor: pointer;
            border-radius: 5px;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(153, 0, 17, 0.3);
        }
        
        .detector-button:hover {
            background: #bb0015;
            transform: scale(1.05);
            box-shadow: 0 8px 25px rgba(153, 0, 17, 0.5);
        }
        
        .detector-result {
            margin-top: 2rem;
            font-size: 1.2rem;
            color: var(--gold);
            min-height: 60px;
            font-weight: bold;
            animation: fadeIn 0.5s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* Contact Form */
        .contact-form {
            background: var(--charcoal);
            padding: 3rem;
            border-radius: 10px;
            max-width: 600px;
            margin: 2rem auto;
            border: 2px solid var(--gold);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            color: var(--gold);
            font-family: 'Oswald', sans-serif;
            margin-bottom: 0.5rem;
            font-size: 1.1rem;
        }
        
        .form-group input,
        .form-group textarea,
        .form-group select {
            width: 100%;
            padding: 0.8rem;
            background: rgba(30, 39, 97, 0.3);
            border: 1px solid var(--cream);
            color: var(--cream);
            font-family: 'Courier Prime', monospace;
            border-radius: 4px;
            font-size: 1rem;
        }
        
        .form-group textarea {
            min-height: 120px;
            resize: vertical;
        }
        
        .submit-button {
            background: var(--gold);
            color: var(--navy);
            border: none;
            padding: 1rem 2rem;
            font-family: 'Oswald', sans-serif;
            font-size: 1.2rem;
            font-weight: bold;
            cursor: pointer;
            border-radius: 5px;
            width: 100%;
            transition: all 0.3s ease;
        }
        
        .submit-button:hover {
            background: #ffd000;
            transform: scale(1.02);
        }
        
        /* Footer */
        footer {
            background: var(--charcoal);
            padding: 2rem;
            text-align: center;
            border-top: 3px solid var(--crimson);
            margin-top: 4rem;
        }
        
        footer p {
            color: var(--cream);
            opacity: 0.8;
        }
        
        .warning-banner {
            background: var(--crimson);
            color: var(--cream);
            padding: 1rem;
            text-align: center;
            font-weight: bold;
            animation: blink 2s infinite;
        }
        
        @keyframes blink {
            0%, 50%, 100% { opacity: 1; }
            25%, 75% { opacity: 0.7; }
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 3rem;
            }
            
            .hero .tagline {
                font-size: 1.3rem;
                letter-spacing: 3px;
            }
            
            .logo {
                font-size: 1.5rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }
        
        /* Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.9);
            z-index: 10000;
            align-items: center;
            justify-content: center;
        }
        
        .modal-content {
            background: var(--charcoal);
            padding: 2rem;
            border-radius: 10px;
            max-width: 500px;
            border: 3px solid var(--crimson);
            position: relative;
            animation: slideIn 0.3s ease;
        }
        
        @keyframes slideIn {
            from { transform: translateY(-50px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        
        .close-modal {
            position: absolute;
            top: 1rem;
            right: 1rem;
            font-size: 2rem;
            color: var(--cream);
            cursor: pointer;
            border: none;
            background: none;
        }
    </style>
</head>
<body>
    <!-- Warning Banner -->
    <div class="warning-banner">
        ⚠️ THIS INFORMATION IS BEING ACTIVELY SUPPRESSED BY GOVERNMENT AGENCIES ⚠️
    </div>

    <!-- Header -->
    <header>
        <div class="header-content">
            <div class="logo">BIRDS AREN'T REAL</div>
            <div class="classified-badge">[CLASSIFIED]</div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <h1>WAKE UP AMERICA</h1>
        <p class="tagline">THE TRUTH THEY DON'T WANT YOU TO KNOW</p>
        <p>Since 1971, the U.S. government has been replacing all birds with surveillance drones. What you see in the sky isn't nature—it's machinery. The evidence is overwhelming. The cover-up is massive. But the truth cannot be silenced forever.</p>
        
        <!-- Bird Counter -->
        <div class="bird-counter">
            <h3>🚨 ACTIVE SURVEILLANCE DRONES DETECTED 🚨</h3>
            <div class="counter-display" id="birdCounter">0</div>
            <div class="counter-label">Real-time drone activity in your area</div>
        </div>
    </section>

    <!-- Evidence Gallery -->
    <section id="evidence">
        <h2 class="section-title">UNDENIABLE EVIDENCE</h2>
        
        <div class="evidence-grid">
            <div class="evidence-card" onclick="showEvidence('power')">
                <div class="evidence-image">⚡</div>
                <div class="evidence-content">
                    <h3>Birds on Power Lines</h3>
                    <p>Why do birds sit on power lines for hours? They're recharging their batteries. It's not complicated—it's just hidden in plain sight.</p>
                </div>
            </div>
            
            <div class="evidence-card" onclick="showEvidence('droppings')">
                <div class="evidence-image">💧</div>
                <div class="evidence-content">
                    <h3>Bird "Droppings"</h3>
                    <p>What you think is waste is actually a liquid tracking apparatus designed to mark your location. Notice how hard it is to clean? That's intentional.</p>
                </div>
            </div>
            
            <div class="evidence-card" onclick="showEvidence('night')">
                <div class="evidence-image">🌙</div>
                <div class="evidence-content">
                    <h3>Complete Shutdown at Night</h3>
                    <p>Birds don't move after dark because the government powers them down to conserve battery life during low-surveillance hours.</p>
                </div>
            </div>
            
            <div class="evidence-card" onclick="showEvidence('babies')">
                <div class="evidence-image">🥚</div>
                <div class="evidence-content">
                    <h3>No Baby Pigeons</h3>
                    <p>When's the last time you saw a baby pigeon? Never. Because the assembly line only produces adult models. This is the smoking gun.</p>
                </div>
            </div>
            
            <div class="evidence-card" onclick="showEvidence('migration')">
                <div class="evidence-image">🧭</div>
                <div class="evidence-content">
                    <h3>"Migration" Patterns</h3>
                    <p>Birds allegedly migrate thousands of miles with perfect accuracy. More likely: GPS-guided drones following programmed routes.</p>
                </div>
            </div>
            
            <div class="evidence-card" onclick="showEvidence('twitter')">
                <div class="evidence-image">🐦</div>
                <div class="evidence-content">
                    <h3>Twitter's Bird Logo</h3>
                    <p>The world's largest social media platform has a bird as its logo. This is how they normalize the surveillance—hiding it in plain sight.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Bird Detector -->
    <section>
        <div class="detector">
            <h3>🔍 ACTIVATE BIRD DETECTOR 🔍</h3>
            <p style="margin-bottom: 1.5rem; color: var(--cream);">Scan your immediate vicinity for government surveillance drones (aka "birds")</p>
            <button class="detector-button" onclick="detectBirds()">SCAN NOW</button>
            <div class="detector-result" id="detectorResult"></div>
        </div>
    </section>

    <!-- Contact Form -->
    <section id="contact">
        <h2 class="section-title">REPORT A SIGHTING</h2>
        <p style="text-align: center; margin-bottom: 2rem; color: var(--cream); opacity: 0.9;">
            Have you witnessed suspicious bird activity? Document it here. Your reports help us build the case.
        </p>
        
        <form class="contact-form" onsubmit="handleSubmit(event)">
            <div class="form-group">
                <label for="name">Name (or remain anonymous):</label>
                <input type="text" id="name" name="name" placeholder="John Doe / Anonymous">
            </div>
            
            <div class="form-group">
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" placeholder="truth-seeker@email.com" required>
            </div>
            
            <div class="form-group">
                <label for="location">Location of Sighting:</label>
                <input type="text" id="location" name="location" placeholder="City, State" required>
            </div>
            
            <div class="form-group">
                <label for="birdType">Type of "Bird" Observed:</label>
                <select id="birdType" name="birdType" required>
                    <option value="">Select Type</option>
                    <option value="pigeon">Pigeon (Standard Urban Surveillance Model)</option>
                    <option value="crow">Crow (Advanced Intelligence Unit)</option>
                    <option value="seagull">Seagull (Coastal Monitoring Drone)</option>
                    <option value="hawk">Hawk (Military-Grade Observer)</option>
                    <option value="robin">Robin (Residential Spy Unit)</option>
                    <option value="other">Other (Experimental Model)</option>
                </select>
            </div>
            
            <div class="form-group">
                <label for="details">Detailed Description:</label>
                <textarea id="details" name="details" placeholder="Describe the suspicious behavior you witnessed..." required></textarea>
            </div>
            
            <button type="submit" class="submit-button">SUBMIT REPORT</button>
        </form>
    </section>

    <!-- Footer -->
    <footer>
        <p style="font-family: 'Bebas Neue', sans-serif; font-size: 1.5rem; color: var(--gold); margin-bottom: 1rem;">
            THE TRUTH IS OUT THERE
        </p>
        <p>© 2025 Birds Aren't Real Movement | Stay Vigilant | If It Flies, It Spies</p>
        <p style="margin-top: 1rem; font-size: 0.9rem; opacity: 0.7;">
            This website is satirical social commentary on conspiracy culture and misinformation.
        </p>
    </footer>

    <!-- Modal -->
    <div class="modal" id="evidenceModal">
        <div class="modal-content">
            <button class="close-modal" onclick="closeModal()">×</button>
            <h3 style="font-family: 'Bebas Neue', sans-serif; color: var(--gold); font-size: 2rem; margin-bottom: 1rem;" id="modalTitle"></h3>
            <p style="color: var(--cream); line-height: 1.6;" id="modalContent"></p>
        </div>
    </div>

    <script>
        // Bird Counter Animation
        let count = 0;
        const targetCount = Math.floor(Math.random() * 500) + 1000;
        const counterElement = document.getElementById('birdCounter');
        
        function animateCounter() {
            if (count < targetCount) {
                count += Math.floor(Math.random() * 50) + 10;
                if (count > targetCount) count = targetCount;
                counterElement.textContent = count.toLocaleString();
                setTimeout(animateCounter, 50);
            }
        }
        
        setTimeout(animateCounter, 500);
        
        // Continuous counter updates
        setInterval(() => {
            const change = Math.floor(Math.random() * 20) - 10;
            count = Math.max(0, count + change);
            counterElement.textContent = count.toLocaleString();
        }, 3000);
        
        // Bird Detector
        const detectorMessages = [
            "⚠️ WARNING: 3 surveillance drones detected within 500ft radius",
            "🚨 ALERT: Pigeon model spotted on nearby rooftop - currently transmitting",
            "⚡ CRITICAL: Crow unit circling overhead - avoid outdoor conversations",
            "🔴 DANGER: Seagull squadron approaching - mass surveillance event imminent",
            "⚠️ CAUTION: Robin detected in tree - home monitoring active",
            "🚨 HIGH ALERT: Multiple hawk units in formation - military operation suspected"
        ];
        
        function detectBirds() {
            const result = document.getElementById('detectorResult');
            result.textContent = "SCANNING...";
            
            setTimeout(() => {
                const message = detectorMessages[Math.floor(Math.random() * detectorMessages.length)];
                result.textContent = message;
            }, 1500);
        }
        
        // Evidence Modal
        const evidenceDetails = {
            power: "Extensive field research has documented birds spending 2-4 hours on power lines daily. Government documentation obtained through FOIA requests reveals power grid modifications in 1972 to support 'avian charging stations.' The correlation is undeniable.",
            droppings: "Chemical analysis of bird droppings reveals traces of lithium-ion compounds and GPS tracking particles. The adhesive properties are far superior to natural biological waste, designed to withstand weather and remain on vehicles for extended periods.",
            night: "Thermal imaging cameras show zero bird activity between 11pm-5am in most urban areas. The synchronization is too perfect to be natural. Government sleep cycles match drone shutdown schedules with 97% accuracy.",
            babies: "The last confirmed sighting of a baby pigeon in a major city was 1973. Population models suggest millions should exist. Where are they? In the factory, being assembled as adult units ready for immediate deployment.",
            migration: "Bird migration patterns follow perfect geometric trajectories that require GPS-level precision. Natural navigation cannot account for this accuracy. Satellite tracking data shows coordinates matching military flight paths.",
            twitter: "Twitter's bird logo was designed in 2006, exactly 35 years after the drone replacement was complete. The company has deep ties to defense contractors. The symbolism is a message: we're watching, and we're not hiding it."
        };
        
        function showEvidence(type) {
            const modal = document.getElementById('evidenceModal');
            const title = document.getElementById('modalTitle');
            const content = document.getElementById('modalContent');
            
            const titles = {
                power: "EVIDENCE FILE #1: Power Line Charging",
                droppings: "EVIDENCE FILE #2: Tracking Liquid Analysis",
                night: "EVIDENCE FILE #3: Nighttime Shutdown Protocol",
                babies: "EVIDENCE FILE #4: The Missing Generation",
                migration: "EVIDENCE FILE #5: GPS Migration Routes",
                twitter: "EVIDENCE FILE #6: Corporate Symbolism"
            };
            
            title.textContent = titles[type];
            content.textContent = evidenceDetails[type];
            modal.style.display = 'flex';
        }
        
        function closeModal() {
            document.getElementById('evidenceModal').style.display = 'none';
        }
        
        // Close modal on outside click
        window.onclick = function(event) {
            const modal = document.getElementById('evidenceModal');
            if (event.target === modal) {
                closeModal();
            }
        }
        
        // Form Submission
        function handleSubmit(event) {
            event.preventDefault();
            
            const form = event.target;
            const formData = new FormData(form);
            
            // Create confirmation message
            const location = formData.get('location');
            const birdType = formData.get('birdType');
            
            alert(`🚨 REPORT RECEIVED 🚨\n\nYour sighting of a ${birdType} in ${location} has been logged.\n\nReport ID: BAR-${Date.now()}\n\nYour contribution to exposing the truth is vital. Stay vigilant.`);
            
            form.reset();
        }
        
        // Easter egg: Konami code
        let konamiCode = ['ArrowUp', 'ArrowUp', 'ArrowDown', 'ArrowDown', 'ArrowLeft', 'ArrowRight', 'ArrowLeft', 'ArrowRight', 'b', 'a'];
        let konamiIndex = 0;
        
        document.addEventListener('keydown', function(e) {
            if (e.key === konamiCode[konamiIndex]) {
                konamiIndex++;
                if (konamiIndex === konamiCode.length) {
                    alert('🔓 CLASSIFIED ACCESS GRANTED\n\nYou have discovered the truth seeker level.\n\nRemember: All birds are drones. All drones are watching. Stay vigilant, comrade.');
                    konamiIndex = 0;
                }
            } else {
                konamiIndex = 0;
            }
        });
    </script>
</body>
</html>
