<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Meli</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&family=Quicksand:wght@300;400;600&family=Cormorant+Garamond:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Quicksand', sans-serif;
            background: linear-gradient(135deg, #ffeef8 0%, #ffe5f1 25%, #fff0f8 50%, #ffeef8 75%, #ffe5f1 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            position: relative;
        }

        .container {
            text-align: center;
            z-index: 10;
            position: relative;
        }

        .text-box {
            background: rgba(255, 255, 255, 0.95);
            padding: 50px 60px;
            border-radius: 30px;
            box-shadow: 0 15px 50px rgba(255, 182, 193, 0.4);
            border: 3px solid #ffc9d9;
            animation: fadeInScale 1s ease-out;
            max-width: 600px;
            position: relative;
            overflow: visible;
        }

        .text-box::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, #ffb6c1, #ffd4e5, #ffe4e1, #ffc9d9);
            border-radius: 30px;
            z-index: -1;
            opacity: 0.3;
        }

        .text-box h1 {
            font-family: 'Dancing Script', cursive;
            font-size: 2.5em;
            color: #d45d79;
            margin-bottom: 30px;
            text-shadow: 2px 2px 4px rgba(212, 93, 121, 0.2);
            line-height: 1.4;
        }

        .text-box p {
            font-size: 1.3em;
            color: #8b5a7d;
            margin-bottom: 20px;
            line-height: 1.8;
        }

        .special-text {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.5em;
            color: #8b5a7d;
            line-height: 1.9;
            font-weight: 400;
        }

        .heart-button {
            width: 100px;
            height: 100px;
            background: transparent;
            border: none;
            cursor: pointer;
            position: relative;
            transition: all 0.3s ease;
            margin-top: 20px;
        }

        .heart-button::before,
        .heart-button::after {
            content: "";
            position: absolute;
            top: 0;
            width: 52px;
            height: 80px;
            background: linear-gradient(135deg, #ff6b9d 0%, #c9507a 100%);
            border-radius: 50px 50px 0 0;
            box-shadow: 0 10px 30px rgba(255, 107, 157, 0.4);
        }

        .heart-button::before {
            left: 50px;
            transform: rotate(-45deg);
            transform-origin: 0 100%;
        }

        .heart-button::after {
            left: 0;
            transform: rotate(45deg);
            transform-origin: 100% 100%;
        }

        .heart-button:hover {
            transform: scale(1.1);
            box-shadow: 0 15px 40px rgba(255, 107, 157, 0.6);
        }

        .heart-button:active {
            transform: scale(0.95);
        }

        .button {
            background: linear-gradient(135deg, #ff6b9d 0%, #c9507a 100%);
            color: white;
            border: none;
            padding: 15px 40px;
            font-size: 1.2em;
            font-family: 'Quicksand', sans-serif;
            font-weight: 600;
            border-radius: 50px;
            cursor: pointer;
            margin: 10px;
            transition: all 0.3s ease;
            box-shadow: 0 5px 20px rgba(255, 107, 157, 0.4);
        }

        .button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(255, 107, 157, 0.6);
        }

        .button:active {
            transform: translateY(0);
        }

        .flower {
            position: absolute;
            font-size: 40px;
            animation: float 4s ease-in-out infinite;
            opacity: 0;
            pointer-events: none;
        }

        .petal {
            position: absolute;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            animation: fall 3s ease-in infinite;
        }

        @keyframes fadeInScale {
            from {
                opacity: 0;
                transform: scale(0.8);
            }
            to {
                opacity: 1;
                transform: scale(1);
            }
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0) translateX(0) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            50% {
                transform: translateY(-100vh) translateX(50px) rotate(180deg);
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-120vh) translateX(0) rotate(360deg);
                opacity: 0;
            }
        }

        @keyframes fall {
            0% {
                transform: translateY(-20px) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(100vh) rotate(720deg);
                opacity: 0.5;
            }
        }

        @keyframes pulse {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.05);
            }
        }

        .hidden {
            display: none;
        }

        .move-away {
            animation: moveAway 0.5s ease-out;
        }

        @keyframes moveAway {
            0% {
                transform: translate(0, 0);
            }
            100% {
                transform: translate(150px, -100px);
            }
        }

        #screen2, #screen3, #screen4 {
            display: none;
        }

        .signature {
            font-family: 'Dancing Script', cursive;
            font-size: 1.8em;
            color: #d45d79;
            margin-top: 30px;
            font-weight: 700;
        }
    </style>
</head>
<body>
    <div id="screen1" class="container">
        <div class="text-box">
            <h1>Meli le tengo una sorpresa</h1>
            <p>Para descubrirla da click sobre el corazón</p>
            <button class="heart-button" onclick="showFlowers()"></button>
        </div>
    </div>

    <div id="screen2" class="container">
        <div class="text-box">
            <h1>Princesa, le complace ser mi San Valentín?</h1>
            <div style="margin-top: 30px;">
                <button class="button" onclick="handleYes()">Si</button>
                <button class="button" id="noButton" onclick="handleNo()">No</button>
            </div>
        </div>
    </div>

    <div id="screen3" class="container">
        <div class="text-box" id="noBox">
            <h1>¿Cómo usted va a decir eso preciosa?</h1>
            <div style="margin-top: 30px;">
                <button class="button" onclick="handleYes()">Es si o si cariño no hay opción</button>
            </div>
        </div>
    </div>

    <div id="screen4" class="container">
        <div class="text-box">
            <h1>Sabía que dirías que si</h1>
            <p class="special-text">Después que Dios hiciera su magia y los caminos se cruzaran, quedó claro algo: quiero vivir este 14 de febrero con usted. Mi corazón, la única fuente confiable en estos temas lo tiene claro desde hace tiempo. Quiero un San Valentín a su lado, lleno de amor, risas sinceras y momentos que se queden grabados en nuestros corazones.</p>
            <button class="button" onclick="showFinal()" style="margin-top: 30px;">Continuar</button>
        </div>
    </div>

    <script>
        function createFlower(x, y) {
            const flowers = ['🌸', '🌺', '🌷', '🌼', '🏵️', '💮'];
            const flower = document.createElement('div');
            flower.className = 'flower';
            flower.textContent = flowers[Math.floor(Math.random() * flowers.length)];
            flower.style.left = x + 'px';
            flower.style.bottom = y + 'px';
            flower.style.animationDelay = Math.random() * 2 + 's';
            document.body.appendChild(flower);

            setTimeout(() => {
                flower.remove();
            }, 4000);
        }

        function createPetal(color) {
            const petal = document.createElement('div');
            petal.className = 'petal';
            petal.style.backgroundColor = color;
            petal.style.left = Math.random() * 100 + '%';
            petal.style.top = '-20px';
            petal.style.animationDelay = Math.random() * 2 + 's';
            petal.style.animationDuration = (Math.random() * 2 + 2) + 's';
            document.body.appendChild(petal);

            setTimeout(() => {
                petal.remove();
            }, 5000);
        }

        function startFlowerAnimation() {
            const colors = ['#ffb6c1', '#ffc9d9', '#ffe4e1', '#ffd4e5', '#ffccdb', '#f8b4d9'];
            
            for (let i = 0; i < 30; i++) {
                setTimeout(() => {
                    createFlower(Math.random() * window.innerWidth, -50);
                }, i * 100);
            }

            for (let i = 0; i < 50; i++) {
                setTimeout(() => {
                    createPetal(colors[Math.floor(Math.random() * colors.length)]);
                }, i * 80);
            }
        }

        function showFlowers() {
            startFlowerAnimation();
            
            setTimeout(() => {
                document.getElementById('screen1').style.display = 'none';
                document.getElementById('screen2').style.display = 'flex';
            }, 2000);
        }

        function handleNo() {
            const noButton = document.getElementById('noButton');
            
            if (!noButton.dataset.clickCount) {
                noButton.dataset.clickCount = 0;
            }
            
            noButton.dataset.clickCount = parseInt(noButton.dataset.clickCount) + 1;
            
            if (noButton.dataset.clickCount < 4) {
                noButton.style.position = 'relative';
                
                const randomX = (Math.random() - 0.5) * 150;
                const randomY = (Math.random() - 0.5) * 80;
                
                noButton.style.transform = `translate(${randomX}px, ${randomY}px)`;
                noButton.style.transition = 'transform 0.3s ease';
            } else {
                document.getElementById('screen2').style.display = 'none';
                document.getElementById('screen3').style.display = 'flex';
            }
        }

        function handleYes() {
            startFlowerAnimation();
            
            setTimeout(() => {
                document.getElementById('screen2').style.display = 'none';
                document.getElementById('screen3').style.display = 'none';
                document.getElementById('screen4').style.display = 'flex';
            }, 2000);
        }

        function showFinal() {
            document.getElementById('screen4').innerHTML = `
                <div class="text-box">
                    <div class="signature">Con mucho amor: Gari</div>
                    <div class="signature" style="margin-top: 20px;">Para la luz de mi alma: Meli</div>
                </div>
            `;
            startFlowerAnimation();
        }

        // Animación de fondo continua
        setInterval(() => {
            if (Math.random() > 0.7) {
                const colors = ['#ffb6c1', '#ffc9d9', '#ffe4e1', '#ffd4e5'];
                createPetal(colors[Math.floor(Math.random() * colors.length)]);
            }
        }, 500);
    </script>
</body>
</html>
