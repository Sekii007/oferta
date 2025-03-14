<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Glitch en sistema...</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background-color: black;
            color: limegreen;
            font-family: monospace;
            font-size: 20px;
            text-align: center;
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }
        .glitch {
            position: absolute;
            font-size: 50px;
            color: red;
            animation: glitchEffect 0.1s infinite;
        }
        @keyframes glitchEffect {
            0% { transform: translate(4px, -4px); }
            25% { transform: translate(-4px, 4px); }
            50% { transform: translate(5px, -5px); }
            75% { transform: translate(-5px, 5px); }
            100% { transform: translate(0, 0); }
        }
        #honkeado {
            display: none;
            background-color: #ffcc00;
            height: 100vh;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
        #honkeado h1 {
            color: red;
            font-size: 40px;
        }
        #honkeado img {
            width: 300px;
            height: auto;
        }
        #mensaje {
            font-size: 16px;
            color: black;
            font-weight: bold;
        }
        #formulario {
            margin-top: 20px;
            padding: 10px 20px;
            background-color: red;
            color: white;
            text-decoration: none;
            font-weight: bold;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <audio id="glitchSound" src="https://www.myinstants.com/media/sounds/glitch.mp3" preload="auto"></audio>
    <div id="glitchText" class="glitch">Error 0x000F5B... SYSTEM FAILURE</div>
    <div id="honkeado">
        <h1>¡Esto es un experimento de clase! 🧪🦆</h1>
        <img src="https://i.imgur.com/MXbXxvF.gif" alt="Honkeado">
        <p id="mensaje">Este experimento no afecta tu dispositivo. Si has pulsado, por favor, rellena este formulario:</p>
        <a id="formulario" href="https://forms.gle/LZhQBEPxdRLwmkQ4A" target="_blank">PULSE AQUÍ</a>
    </div>
    <script>
        let glitchText = document.getElementById("glitchText");
        let sound = document.getElementById("glitchSound");
        let mensajes = [
            "Restableciendo BIOS...",
            "Conectando al servidor...",
            "Acceso no autorizado...",
            "Borrando archivos...",
            "Error crítico del sistema...",
            "Instalando virus.exe...",
            "Hack en progreso..."
        ];
        let glitchInterval = setInterval(() => {
            let randomIndex = Math.floor(Math.random() * mensajes.length);
            glitchText.textContent = mensajes[randomIndex];
        }, 200);
        sound.play();
        setTimeout(() => {
            clearInterval(glitchInterval);
            document.body.style.backgroundColor = "#ffcc00";
            glitchText.style.display = "none";
            document.getElementById("honkeado").style.display = "flex";
        }, 3500);
    </script>
</body>
</html>
