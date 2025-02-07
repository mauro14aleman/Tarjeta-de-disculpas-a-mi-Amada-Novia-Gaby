<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Ti 💜</title>
    <style>
        body {
            background: linear-gradient(to right, #ff9a9e, #fad0c4);
            color: white;
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 50px;
            overflow: hidden;
            position: relative;
        }
        .card {
            background: rgba(255, 255, 255, 0.2);
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            max-width: 500px;
            margin: auto;
        }
        .video-container {
            margin-top: 20px;
        }
        .btn {
            background: #ff69b4;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            margin-top: 10px;
        }
        .btn:hover {
            background: #ff1493;
        }
        .hearts, .flowers {
            position: absolute;
            animation: float 4s infinite ease-in-out;
        }
        @keyframes float {
            0% { transform: translateY(0); opacity: 1; }
            50% { transform: translateY(-20px); opacity: 0.7; }
            100% { transform: translateY(0); opacity: 1; }
        }
    </style>
</head>
<body>
    <div class="card">
        <h1>Para Ti mi hermosa novia💜</h1>
        <p>Hoy es un día especial, porque tú lo haces especial aunque no te vea a diario . Eres mi felicidad, mi paz y mi amor a diario
        y un dia podremos ver juntos en la tele la cancion que tanto te encanta, sonrie mi amor eres hermosa. 💖🌸</p>
        <div class="video-container">
            <iframe width="400" height="225" src="https://www.youtube.com/embed/3aB41fwBvmA" frameborder="0" allowfullscreen></iframe>
        </div>
    </div>
    
    <script>
        function createAnimation(className, emoji) {
            for (let i = 0; i < 15; i++) {
                let element = document.createElement('div');
                element.className = className;
                element.innerHTML = emoji;
                element.style.left = Math.random() * 100 + 'vw';
                element.style.top = Math.random() * 100 + 'vh';
                element.style.fontSize = Math.random() * 30 + 20 + 'px';
                element.style.position = 'absolute';
                document.body.appendChild(element);
                setInterval(() => {
                    element.style.top = Math.random() * 100 + 'vh';
                    element.style.left = Math.random() * 100 + 'vw';
                }, 3000);
            }
        }
        createAnimation('hearts', '💖');
        createAnimation('flowers', '🌸');
    </script>
</body>
</html>

