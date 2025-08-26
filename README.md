<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Feliz 7º Dia B</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Georgia', serif;
        }
        
        body {
            background-color: #fff5f5;
            color: #333;
            line-height: 1.6;
            padding: 15px;
            background-image: linear-gradient(to bottom, #ffe6e6, #fff5f5);
            overflow-x: hidden;
            min-height: 100vh;
        }
        
        .container {
            max-width: 100%;
            margin: 0 auto;
            background-color: white;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 0 15px rgba(0,0,0,0.1);
            position: relative;
            z-index: 1;
        }
        
        header {
            text-align: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid #ff9999;
            position: relative;
            height: 80px;
            overflow: hidden;
        }
        
        .blinking-text {
            color: #cc0066;
            font-size: 1.8rem;
            font-weight: bold;
            position: absolute;
            animation: blink 2s infinite, move 15s infinite alternate;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
            white-space: nowrap;
        }
        
        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.3; }
        }
        
        @keyframes move {
            0% { left: 5%; transform: translateY(0) rotate(-2deg); }
            25% { left: 50%; transform: translateY(15px) rotate(2deg); }
            50% { left: 20%; transform: translateY(30px) rotate(-3deg); }
            75% { left: 60%; transform: translateY(15px) rotate(3deg); }
            100% { left: 5%; transform: translateY(0) rotate(-2deg); }
        }
        
        h2 {
            color: #cc0066;
            margin: 20px 0 15px;
            padding-bottom: 5px;
            border-bottom: 1px dashed #ff9999;
            font-size: 1.5rem;
        }
        
        .intro {
            font-style: italic;
            text-align: center;
            margin-bottom: 20px;
            color: #666;
            font-size: 1rem;
        }
        
        .recipe-section {
            margin-bottom: 25px;
        }
        
        .recipe-step {
            margin-bottom: 20px;
            padding-left: 5px;
        }
        
        .recipe-step h3 {
            color: #99004d;
            margin-bottom: 5px;
            font-size: 1.2rem;
        }
        
        .recipe-step p {
            margin-left: 15px;
            margin-bottom: 8px;
            font-size: 0.95rem;
        }
        
        .photo-section {
            text-align: center;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 2px solid #ff9999;
        }
        
        .photo-container {
            width: 280px;
            height: 280px;
            margin: 15px auto;
            border: 3px solid #ff9999;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .our-photo {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        footer {
            text-align: center;
            margin-top: 25px;
            color: #999;
            font-size: 0.85rem;
        }
        
        .floating-hearts {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
        }
        
        .heart {
            position: absolute;
            font-size: 18px;
            color: rgba(255, 105, 180, 0.5);
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 0;
            }
            50% {
                opacity: 0.6;
            }
            100% {
                transform: translateY(-100vh) rotate(360deg);
                opacity: 0;
            }
        }
        
        /* Melhorias para mobile */
        @media (max-width: 480px) {
            body {
                padding: 10px;
                font-size: 14px;
            }
            
            .container {
                padding: 15px;
            }
            
            .blinking-text {
                font-size: 1.5rem;
            }
            
            .photo-container {
                width: 220px;
                height: 220px;
            }
            
            h2 {
                font-size: 1.3rem;
            }
            
            .recipe-step h3 {
                font-size: 1.1rem;
            }
        }
        
        /* Para telas muito pequenas */
        @media (max-width: 320px) {
            .blinking-text {
                font-size: 1.3rem;
            }
            
            .photo-container {
                width: 200px;
                height: 200px;
            }
        }
        
        /* Botão de voltar ao topo */
        .back-to-top {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: #cc0066;
            color: white;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 20px;
            cursor: pointer;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
            z-index: 1000;
            opacity: 0;
            transition: opacity 0.3s;
        }
        
        .back-to-top.show {
            opacity: 1;
        }
        
        .photo-caption {
            margin-top: 10px;
            font-style: italic;
            color: #cc0066;
        }
    </style>
</head>
<body>
    <div class="floating-hearts" id="hearts"></div>
    
    <div class="container">
        <header>
            <div class="blinking-text">Feliz 7º Dia B</div>
        </header>
        
        <p class="intro">Um presente especial para renovar energias e celebrar a vida</p>
        
        <div class="recipe-section">
            <h2>Banho de Rosa - Ritual de Transformação</h2>
            
            <div class="recipe-step">
                <h3>1. Escolha da rosa</h3>
                <p>– Vermelha → amor e força vital.</p>
            </div>
            
            <div class="recipe-step">
                <h3>2. Preparação</h3>
                <p>– Colhe as pétalas com respeito (não arranca de qualquer jeito).</p>
                <p>– Agradece à planta — a alquimia sempre pede reconhecimento à vida que cede.</p>
                <p>– Usa água limpa (se possível de fonte, chuva ou mineral).</p>
            </div>
            
            <div class="recipe-step">
                <h3>3. Ativação</h3>
                <p>– Coloca as pétalas na água morna, não fervendo.</p>
                <p>– Enquanto a água aquece, mexe em sentido horário (atração, abertura) ou anti-horário (limpeza, banimento).</p>
                <p>– Sopra três vezes sobre a água, pensando no que quer trazer ou afastar.</p>
            </div>
            
            <div class="recipe-step">
                <h3>4. O banho</h3>
                <p>– Depois do banho normal, derrama a água de pétalas do pescoço pra baixo.</p>
                <p>– Não enxágua depois — deixa secar no corpo.</p>
                <p>– Enquanto derrama, fala um verbo de poder (ex: "que caia o velho, que floresça o novo").</p>
            </div>
            
            <div class="recipe-step">
                <h3>5. Finalização</h3>
                <p>– As pétalas usadas não vão pro lixo: devolve à terra ou a um jardim.</p>
                <p>– A energia fecha o ciclo quando volta ao chão.</p>
            </div>
        </div>
        
        <div class="photo-section">
            <h2>Nossa Foto Especial</h2>
            <div class="photo-container">
                <img src="https://i.ibb.co/6n60L9P/IMG-20241006-211136-862.jpg" alt="Nossa foto especial" class="our-photo">
            </div>
            <p class="photo-caption">Este momento especial merece ser lembrado para sempre</p>
        </div>
        
        <footer>
            <p>Com carinho, um presente para energizar sua alma</p>
        </footer>
    </div>

    <div class="back-to-top" id="backToTop">↑</div>

    <script>
        // Criar corações flutuantes
        function createHearts() {
            const heartsContainer = document.getElementById('hearts');
            const numberOfHearts = 20;
            
            for (let i = 0; i < numberOfHearts; i++) {
                const heart = document.createElement('div');
                heart.innerHTML = '❤';
                heart.classList.add('heart');
                
                // Posição aleatória
                heart.style.left = Math.random() * 100 + 'vw';
                heart.style.animationDelay = Math.random() * 5 + 's';
                heart.style.fontSize = (Math.random() * 12 + 8) + 'px';
                
                heartsContainer.appendChild(heart);
            }
        }
        
        // Botão de voltar ao topo
        function setupBackToTop() {
            const backToTopButton = document.getElementById('backToTop');
            
            window.addEventListener('scroll', () => {
                if (window.scrollY > 300) {
                    backToTopButton.classList.add('show');
                } else {
                    backToTopButton.classList.remove('show');
                }
            });
            
            backToTopButton.addEventListener('click', () => {
                window.scrollTo({
                    top: 0,
                    behavior: 'smooth'
                });
            });
        }
        
        // Iniciar quando a página carregar
        window.onload = function() {
            createHearts();
            setupBackToTop();
            
            // Garantir que a imagem seja carregada
            const img = new Image();
            img.src = "https://i.ibb.co/6n60L9P/IMG-20241006-211136-862.jpg";
        };
    </script>
</body>
</html>
