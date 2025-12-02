<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Hamna! 🎉</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #0f0f23 0%, #1a1a2e 50%, #16213e 100%);
            color: #e8e8f0;
            overflow-x: hidden;
            min-height: 100vh;
        }

        .doremon-container {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
            z-index: 1000;
            cursor: pointer;
        }

        .doremon {
            font-size: clamp(5rem, 15vw, 8rem);
            animation: bounce 2s infinite;
            margin-bottom: 1rem;
        }

        .board {
            background: #fff;
            color: #333;
            padding: clamp(1rem, 4vw, 2rem);
            border-radius: 15px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
            font-family: 'Playfair Display', serif;
            font-size: clamp(1rem, 3vw, 1.5rem);
            max-width: 90vw;
        }

        .flowers-in-hand {
            position: absolute;
            top: -20px;
            right: -30px;
            font-size: clamp(2rem, 6vw, 3rem);
            animation: wave 1.5s ease-in-out infinite;
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-20px); }
            60% { transform: translateY(-10px); }
        }

        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            50% { transform: rotate(15deg); }
        }

        .countdown-container {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
            z-index: 1000;
            display: none;
        }

        .countdown-number {
            font-size: clamp(4rem, 15vw, 8rem);
            font-weight: bold;
            color: #ff6b9d;
            text-shadow: 0 0 50px rgba(255, 107, 157, 0.8);
            margin-bottom: 1rem;
        }

        .countdown-text {
            font-family: 'Playfair Display', serif;
            font-size: clamp(1.2rem, 4vw, 2rem);
            color: #4ecdc4;
            text-shadow: 0 0 20px rgba(78, 205, 196, 0.5);
        }

        .flowers-display {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
            z-index: 1000;
            display: none;
            animation: flowerBloom 3s ease-out;
        }

        .red-flowers {
            font-size: clamp(3rem, 12vw, 6rem);
            margin-bottom: 2rem;
            animation: flowerSway 2s ease-in-out infinite;
        }

        .birthday-message {
            font-family: 'Playfair Display', serif;
            font-size: clamp(1.5rem, 5vw, 3rem);
            background: linear-gradient(45deg, #ff6b9d, #ffd700, #4ecdc4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 30px rgba(255, 107, 157, 0.5);
        }

        @keyframes flowerBloom {
            0% { opacity: 0; transform: translate(-50%, -50%) scale(0.3); }
            100% { opacity: 1; transform: translate(-50%, -50%) scale(1); }
        }

        @keyframes flowerSway {
            0%, 100% { transform: rotate(-5deg); }
            50% { transform: rotate(5deg); }
        }

        .main-content {
            display: none;
            padding: clamp(1rem, 4vw, 2rem);
            max-width: 1200px;
            margin: 0 auto;
            position: relative;
            z-index: 2;
        }

        .love-message {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: clamp(2rem, 5vw, 3rem);
            margin: 2rem 0;
            text-align: center;
            border: 1px solid rgba(255, 107, 157, 0.3);
        }

        .love-message h3 {
            font-family: 'Playfair Display', serif;
            font-size: clamp(1.5rem, 4vw, 2rem);
            color: #ff6b9d;
            margin-bottom: 2rem;
        }

        .love-message p {
            font-size: clamp(1rem, 3vw, 1.2rem);
            line-height: 1.8;
            margin-bottom: 1.5rem;
        }

        .urdu-love {
            font-size: clamp(1.1rem, 3vw, 1.3rem);
            color: #4ecdc4;
            font-style: italic;
            direction: rtl;
            text-align: right;
        }

        /* Wish Tree */
        .wish-tree-section {
            text-align: center;
            margin: 3rem 0;
            padding: clamp(1.5rem, 4vw, 2rem);
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
        }

        .tree {
            font-size: clamp(6rem, 15vw, 10rem);
            margin: 2rem 0;
            position: relative;
            display: inline-block;
        }

        .wish-leaves {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }

        .leaf {
            position: absolute;
            font-size: clamp(1.5rem, 4vw, 2rem);
            cursor: pointer;
            animation: leafSway 3s ease-in-out infinite;
            transition: transform 0.3s ease;
        }

        .leaf:hover {
            transform: scale(1.3);
        }

        @keyframes leafSway {
            0%, 100% { transform: rotate(-5deg); }
            50% { transform: rotate(5deg); }
        }

        .wish-popup {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: rgba(255, 255, 255, 0.95);
            color: #333;
            padding: clamp(1.5rem, 4vw, 2rem);
            border-radius: 15px;
            max-width: 90vw;
            display: none;
            z-index: 1001;
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
            text-align: center;
        }

        /* Interactive Birthday Cake */
        .birthday-cake-section {
            text-align: center;
            margin: 3rem 0;
            padding: clamp(1.5rem, 4vw, 2rem);
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
        }

        .cake {
            font-size: clamp(5rem, 12vw, 8rem);
            cursor: pointer;
            transition: transform 0.3s ease;
            position: relative;
        }

        .cake:hover {
            transform: scale(1.1);
        }

        .candles {
            position: absolute;
            top: -20px;
            left: 50%;
            transform: translateX(-50%);
            font-size: clamp(1.5rem, 4vw, 2rem);
        }

        .cake-message {
            margin-top: 1rem;
            font-family: 'Playfair Display', serif;
            font-size: clamp(1.2rem, 3vw, 1.5rem);
            color: #ff6b9d;
        }

        /* Promise Rings */
        .rings-section {
            text-align: center;
            margin: 3rem 0;
            padding: clamp(1.5rem, 4vw, 2rem);
        }

        .rings-container {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: clamp(1rem, 4vw, 2rem);
            margin: 2rem 0;
            flex-wrap: wrap;
        }

        .ring {
            font-size: clamp(3rem, 8vw, 4rem);
            animation: ringFloat 3s ease-in-out infinite;
            cursor: pointer;
        }

        .ring:nth-child(2) {
            animation-delay: -1.5s;
        }

        .rings-together {
            font-size: clamp(4rem, 10vw, 6rem);
            display: none;
            animation: ringUnite 2s ease-out;
        }

        @keyframes ringFloat {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
        }

        @keyframes ringUnite {
            0% { opacity: 0; transform: scale(0.5); }
            100% { opacity: 1; transform: scale(1); }
        }

        /* Floating Love Letters */
        .love-letters {
            position: fixed;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 10;
        }

        .letter {
            position: absolute;
            font-size: clamp(1.5rem, 4vw, 2rem);
            cursor: pointer;
            pointer-events: all;
            animation: letterFloat 6s ease-in-out infinite;
            transition: transform 0.3s ease;
        }

        .letter:hover {
            transform: scale(1.2);
        }

        @keyframes letterFloat {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            25% { transform: translateY(-20px) rotate(5deg); }
            50% { transform: translateY(-10px) rotate(-3deg); }
            75% { transform: translateY(-15px) rotate(2deg); }
        }

        .letter-content {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: rgba(255, 255, 255, 0.95);
            color: #333;
            padding: clamp(1.5rem, 4vw, 2rem);
            border-radius: 15px;
            max-width: 90vw;
            display: none;
            z-index: 1001;
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
        }

        /* Fireworks */
        .fireworks {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 5;
        }

        .firework {
            position: absolute;
            width: 4px;
            height: 4px;
            border-radius: 50%;
            animation: explode 2s ease-out;
        }

        @keyframes explode {
            0% { transform: scale(0); opacity: 1; }
            50% { transform: scale(1); opacity: 0.8; }
            100% { transform: scale(2); opacity: 0; }
        }

        /* Heart Rain */
        .heart-rain {
            position: fixed;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 3;
        }

        .heart {
            position: absolute;
            font-size: clamp(1rem, 3vw, 1.5rem);
            animation: heartFall 4s linear infinite;
            cursor: pointer;
            pointer-events: all;
        }

        @keyframes heartFall {
            0% { transform: translateY(-100vh) rotate(0deg); opacity: 1; }
            100% { transform: translateY(100vh) rotate(360deg); opacity: 0; }
        }

        .stars {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }

        .star {
            position: absolute;
            width: 2px;
            height: 2px;
            background: #ffd700;
            border-radius: 50%;
            animation: twinkle 3s infinite;
        }

        @keyframes twinkle {
            0%, 100% { opacity: 0.3; }
            50% { opacity: 1; }
        }

        .confetti {
            position: fixed;
            width: 10px;
            height: 10px;
            background: #ff6b9d;
            animation: fall 4s linear infinite;
            z-index: 1;
        }

        @keyframes fall {
            0% { transform: translateY(-100vh) rotate(0deg); opacity: 1; }
            100% { transform: translateY(100vh) rotate(360deg); opacity: 0; }
        }

        /* Mobile Responsive */
        @media (max-width: 768px) {
            .rings-container {
                flex-direction: column;
                gap: 1rem;
            }
            
            .leaf {
                font-size: 1.2rem;
            }
            
            .letter-content, .wish-popup {
                margin: 1rem;
                max-width: calc(100vw - 2rem);
            }
        }

        @media (max-width: 480px) {
            .main-content {
                padding: 1rem;
            }
            
            .love-message {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="stars"></div>
    <div class="heart-rain" id="heartRain"></div>
    <div class="love-letters" id="loveLetters"></div>
    <div class="fireworks" id="fireworks"></div>
    
    <div class="doremon-container" id="doremonContainer">
        <div class="doremon">🤖</div>
        <div class="flowers-in-hand">💐</div>
        <div class="board">
            I have a surprise for you!<br>
            Hit me to get it! 💕
        </div>
    </div>

    <div class="countdown-container" id="countdownContainer">
        <div class="countdown-number" id="countdownNumber">10</div>
        <div class="countdown-text" id="countdownText">Hyee Princess</div>
    </div>

    <div class="flowers-display" id="flowersDisplay">
        <div class="red-flowers">🌹🌹🌹🌹🌹</div>
        <div class="birthday-message">
            Happy Birthday Hamna!<br>
            Many Many Returns! 🎂💖
        </div>
    </div>

    <div class="main-content" id="mainContent">
        <div class="love-message">
            <h3>My Dearest Moti 💕</h3>
            <p>
                You are absolutely special, everything best in this world! You are the one 
                <strong>jis ka khayal mere zehan mein rehta hai</strong> day and night. 
                I want to see you as my wife in my future, Moti. You are my dream, my happiness, my everything!
            </p>
            <p>
                After 5 years when we met again, my heart knew you were meant to be mine. 
                I know you don't have feelings for me yet, but I believe in our destiny. 
                You said yes to our future, and that gives me hope!
            </p>
            <p class="urdu-love">
                تم میری زندگی کا سب سے خوبصورت خواب ہو، میری جان حمنہ! 
                اللہ کرے یہ جنم دن تمہارے لیے بہت خوشیاں لے کر آئے۔ 
                میں انتظار کروں گا جب تک تمہارا دل میرے لیے محبت سے نہ بھر جائے۔
            </p>
            <p>
                Happy Birthday my future wife! May Allah bless you with all the happiness in the world. 
                You're going to be an amazing software engineer, and I'll be there to support all your dreams! 
                🎂👑💖
            </p>
        </div>

        <div class="wish-tree-section">
            <h3 style="color: #ff6b9d; font-family: 'Playfair Display', serif; margin-bottom: 2rem;">Wish Tree for My Princess 🌳</h3>
            <p style="color: #4ecdc4; margin-bottom: 2rem;">Click on the leaves to see my wishes for you!</p>
            <div class="tree">
                🌳
                <div class="wish-leaves">
                    <div class="leaf" style="top: 10%; left: 20%;" onclick="showWish('May Allah bless you with endless happiness and success in everything you do, my beautiful Moti! 🌟')">🍃</div>
                    <div class="leaf" style="top: 15%; right: 25%;" onclick="showWish('I wish for the day when your heart will be filled with love for me, just like mine is for you! 💕')">🍃</div>
                    <div class="leaf" style="top: 25%; left: 15%;" onclick="showWish('May your software engineering career reach new heights and bring you immense joy! 👩‍💻✨')">🍃</div>
                    <div class="leaf" style="top: 30%; right: 20%;" onclick="showWish('I wish we create beautiful memories together as husband and wife in the future! 💍👫')">🍃</div>
                    <div class="leaf" style="top: 20%; left: 50%;" onclick="showWish('تمہاری ہر خوشی میری خوشی ہے، میری جان! (Your every happiness is my happiness, my life!) 🌹')">🍃</div>
                    <div class="leaf" style="top: 35%; right: 45%;" onclick="showWish('May Allah protect you always and keep you smiling, my precious Doremon! 😊🤲')">🍃</div>
                    <div class="leaf" style="top: 40%; left: 30%;" onclick="showWish('I wish for countless birthdays together, celebrating our love and dreams! 🎂💖')">🍃</div>
                    <div class="leaf" style="top: 45%; right: 35%;" onclick="showWish('May every line of code you write bring you closer to your dreams, my brilliant princess! 💻🌟')">🍃</div>
                </div>
            </div>
        </div>

        <div class="birthday-cake-section">
            <h3 style="color: #ff6b9d; font-family: 'Playfair Display', serif; margin-bottom: 2rem;">Make a Wish & Blow the Candles! 🕯️</h3>
            <div class="cake" id="birthdayCake">
                <div class="candles">🕯️🕯️🕯️</div>
                🎂
            </div>
            <div class="cake-message" id="cakeMessage">Click the cake to blow out candles!</div>
        </div>

        <div class="rings-section">
            <h3 style="color: #ff6b9d; font-family: 'Playfair Display', serif; margin-bottom: 2rem;">Our Promise Rings 💍</h3>
            <div class="rings-container" id="ringsContainer">
                <div class="ring" onclick="uniteRings()">💍</div>
                <div style="color: #4ecdc4; font-size: clamp(1.5rem, 4vw, 2rem);">+</div>
                <div class="ring" onclick="uniteRings()">💍</div>
            </div>
            <div class="rings-together" id="ringsTogether">💕💍💍💕</div>
            <p style="color: #4ecdc4; margin-top: 1rem;">Click the rings to unite our future!</p>
        </div>
    </div>

    <div class="letter-content" id="letterContent">
        <h4 style="color: #ff6b9d; margin-bottom: 1rem;">Love Letter 💌</h4>
        <p id="letterText">Click outside to close</p>
        <button onclick="closeLetter()" style="margin-top: 1rem; padding: 0.5rem 1rem; background: #ff6b9d; color: white; border: none; border-radius: 5px; cursor: pointer;">Close</button>
    </div>

    <div class="wish-popup" id="wishPopup">
        <h4 style="color: #ff6b9d; margin-bottom: 1rem;">My Wish for You 🌟</h4>
        <p id="wishText"></p>
        <button onclick="closeWish()" style="margin-top: 1rem; padding: 0.5rem 1rem; background: #ff6b9d; color: white; border: none; border-radius: 5px; cursor: pointer;">Close</button>
    </div>

    <script>
        // Create stars
        function createStars() {
            const starsContainer = document.querySelector('.stars');
            for (let i = 0; i < 100; i++) {
                const star = document.createElement('div');
                star.className = 'star';
                star.style.left = Math.random() * 100 + '%';
                star.style.top = Math.random() * 100 + '%';
                star.style.animationDelay = Math.random() * 3 + 's';
                starsContainer.appendChild(star);
            }
        }

        // Create confetti
        function createConfetti() {
            for (let i = 0; i < 30; i++) {
                setTimeout(() => {
                    const confetti = document.createElement('div');
                    confetti.className = 'confetti';
                    confetti.style.left = Math.random() * 100 + '%';
                    confetti.style.backgroundColor = ['#ff6b9d', '#4ecdc4', '#ffd700', '#667eea'][Math.floor(Math.random() * 4)];
                    confetti.style.animationDelay = Math.random() * 2 + 's';
                    document.body.appendChild(confetti);
                    
                    setTimeout(() => confetti.remove(), 4000);
                }, i * 100);
            }
        }

        // Create heart rain
        function createHeartRain() {
            const heartRain = document.getElementById('heartRain');
            for (let i = 0; i < 15; i++) {
                setTimeout(() => {
                    const heart = document.createElement('div');
                    heart.className = 'heart';
                    heart.textContent = ['💖', '💕', '💝', '💗'][Math.floor(Math.random() * 4)];
                    heart.style.left = Math.random() * 100 + '%';
                    heart.style.animationDelay = Math.random() * 2 + 's';
                    heart.onclick = () => {
                        heart.style.animation = 'explode 0.5s ease-out';
                        setTimeout(() => heart.remove(), 500);
                    };
                    heartRain.appendChild(heart);
                    
                    setTimeout(() => heart.remove(), 4000);
                }, i * 300);
            }
        }

        // Create floating love letters
        function createLoveLetters() {
            const letters = ['💌', '💌', '💌', '💌', '💌'];
            const messages = [
                'Moti, you are my everything! 💕',
                'Doremon, I love you more each day! 💖',
                'You make my heart skip a beat! 💓',
                'Can\'t wait to call you my wife! 💍',
                'تم میری زندگی ہو! (You are my life!) 🌹'
            ];
            
            letters.forEach((letter, index) => {
                setTimeout(() => {
                    const letterEl = document.createElement('div');
                    letterEl.className = 'letter';
                    letterEl.textContent = letter;
                    letterEl.style.left = Math.random() * 80 + 10 + '%';
                    letterEl.style.top = Math.random() * 80 + 10 + '%';
                    letterEl.style.animationDelay = Math.random() * 3 + 's';
                    letterEl.onclick = () => openLetter(messages[index]);
                    document.getElementById('loveLetters').appendChild(letterEl);
                }, index * 2000);
            });
        }

        // Show wish from tree
        function showWish(wishText) {
            document.getElementById('wishText').textContent = wishText;
            document.getElementById('wishPopup').style.display = 'block';
        }

        // Close wish popup
        function closeWish() {
            document.getElementById('wishPopup').style.display = 'none';
        }

        // Open love letter
        function openLetter(message) {
            document.getElementById('letterText').textContent = message;
            document.getElementById('letterContent').style.display = 'block';
        }

        // Close love letter
        function closeLetter() {
            document.getElementById('letterContent').style.display = 'none';
        }

        // Create fireworks
        function createFireworks() {
            for (let i = 0; i < 20; i++) {
                setTimeout(() => {
                    const firework = document.createElement('div');
                    firework.className = 'firework';
                    firework.style.left = Math.random() * 100 + '%';
                    firework.style.top = Math.random() * 100 + '%';
                    firework.style.backgroundColor = ['#ff6b9d', '#4ecdc4', '#ffd700', '#667eea'][Math.floor(Math.random() * 4)];
                    document.getElementById('fireworks').appendChild(firework);
                    
                    setTimeout(() => firework.remove(), 2000);
                }, i * 100);
            }
        }

        // Birthday cake interaction
        document.getElementById('birthdayCake').onclick = function() {
            this.innerHTML = '🎂';
            document.getElementById('cakeMessage').textContent = 'Wish granted! Happy Birthday Moti! 🎉';
            createFireworks();
        };

        // Unite rings
        function uniteRings() {
            document.getElementById('ringsContainer').style.display = 'none';
            document.getElementById('ringsTogether').style.display = 'block';
            createFireworks();
        }

        // Play beep sound
        function playBeep() {
            const audioContext = new (window.AudioContext || window.webkitAudioContext)();
            const oscillator = audioContext.createOscillator();
            const gainNode = audioContext.createGain();
            
            oscillator.connect(gainNode);
            gainNode.connect(audioContext.destination);
            
            oscillator.frequency.value = 800;
            oscillator.type = 'sine';
            
            gainNode.gain.setValueAtTime(0.3, audioContext.currentTime);
            gainNode.gain.exponentialRampToValueAtTime(0.01, audioContext.currentTime + 0.5);
            
            oscillator.start(audioContext.currentTime);
            oscillator.stop(audioContext.currentTime + 0.5);
        }

        // Doremon click handler
        document.getElementById('doremonContainer').addEventListener('click', function() {
            this.style.display = 'none';
            
            // Start countdown
            const countdownContainer = document.getElementById('countdownContainer');
            const countdownNumber = document.getElementById('countdownNumber');
            const countdownText = document.getElementById('countdownText');
            
            countdownContainer.style.display = 'block';
            
            const messages = [
                'Hyee Princess',
                'Hyee Moto', 
                'Hyee Charming',
                'Hi Catoo',
                'Hi Beautiful',
                'Hi Gorgeous',
                'Hi Stunning',
                'Hi Cute',
                'Hi My Love',
                'Hi Future Wife'
            ];
            
            let count = 10;
            const countdownInterval = setInterval(() => {
                playBeep();
                countdownNumber.textContent = count;
                countdownText.textContent = messages[10 - count] || 'Hi Princess';
                count--;
                
                if (count < 0) {
                    clearInterval(countdownInterval);
                    countdownContainer.style.display = 'none';
                    
                    // Show flowers and play Happy Birthday tune
                    document.getElementById('flowersDisplay').style.display = 'block';
                    createConfetti();
                    playHappyBirthdayTune();
                    
                    // Continue playing Happy Birthday tune periodically
                    setInterval(playHappyBirthdayTune, 25000);
                    
                    // Show main content after flowers
                    setTimeout(() => {
                        document.getElementById('flowersDisplay').style.display = 'none';
                        document.getElementById('mainContent').style.display = 'block';
                        
                        // Start interactive elements
                        setTimeout(() => {
                            createHeartRain();
                            createLoveLetters();
                        }, 2000);
                    }, 5000);
                }
            }, 1000);
        });

        // Happy Birthday tune
        function playHappyBirthdayTune() {
            const audioContext = new (window.AudioContext || window.webkitAudioContext)();
            
            // Happy Birthday melody notes
            const melody = [
                { freq: 261.63, start: 0, duration: 0.5 },    // C - Hap-
                { freq: 261.63, start: 0.5, duration: 0.5 },  // C - py
                { freq: 293.66, start: 1.0, duration: 1.0 },  // D - Birth-
                { freq: 261.63, start: 2.0, duration: 1.0 },  // C - day
                { freq: 349.23, start: 3.0, duration: 1.0 },  // F - to
                { freq: 329.63, start: 4.0, duration: 2.0 },  // E - you
                
                { freq: 261.63, start: 6.5, duration: 0.5 },  // C - Hap-
                { freq: 261.63, start: 7.0, duration: 0.5 },  // C - py
                { freq: 293.66, start: 7.5, duration: 1.0 },  // D - Birth-
                { freq: 261.63, start: 8.5, duration: 1.0 },  // C - day
                { freq: 392.00, start: 9.5, duration: 1.0 },  // G - to
                { freq: 349.23, start: 10.5, duration: 2.0 }, // F - you
                
                { freq: 261.63, start: 13.0, duration: 0.5 }, // C - Hap-
                { freq: 261.63, start: 13.5, duration: 0.5 }, // C - py
                { freq: 523.25, start: 14.0, duration: 1.0 }, // C5 - Birth-
                { freq: 440.00, start: 15.0, duration: 1.0 }, // A - day
                { freq: 349.23, start: 16.0, duration: 1.0 }, // F - dear
                { freq: 329.63, start: 17.0, duration: 1.0 }, // E - Ham-
                { freq: 293.66, start: 18.0, duration: 2.0 }, // D - na
            ];
            
            melody.forEach(note => {
                const oscillator = audioContext.createOscillator();
                const gainNode = audioContext.createGain();
                
                oscillator.connect(gainNode);
                gainNode.connect(audioContext.destination);
                
                oscillator.frequency.setValueAtTime(note.freq, audioContext.currentTime + note.start);
                oscillator.type = 'triangle';
                
                gainNode.gain.setValueAtTime(0, audioContext.currentTime + note.start);
                gainNode.gain.linearRampToValueAtTime(0.15, audioContext.currentTime + note.start + 0.1);
                gainNode.gain.linearRampToValueAtTime(0.15, audioContext.currentTime + note.start + note.duration - 0.1);
                gainNode.gain.linearRampToValueAtTime(0, audioContext.currentTime + note.start + note.duration);
                
                oscillator.start(audioContext.currentTime + note.start);
                oscillator.stop(audioContext.currentTime + note.start + note.duration);
            });
        }

        // Initialize
        createStars();
        
        // Happy Birthday tune will play after countdown
        
        // Periodic effects
        setTimeout(() => {
            setInterval(createConfetti, 8000);
            setInterval(createHeartRain, 12000);
        }, 20000);
    </script>
</body>
</html>
