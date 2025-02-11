<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Te Amo Gabriela</title>
    <style>
        body {
            margin: 0;
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            font-family: 'Comic Sans MS', cursive, sans-serif;
            text-align: center;
            transition: background 0.5s;
        }
        .text {
            font-size: 2em;
            color: #fff;
            text-shadow: 0 0 10px #ff00ff, 0 0 20px #ff66ff;
        }
        .heart {
            position: absolute;
            color: red;
            font-size: 1.5em;
            animation: float 1.5s linear infinite;
        }
        @keyframes float {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(-100px); opacity: 0; }
        }
    </style>
</head>
<body onclick="nextScreen(event)">
    <div class="text" id="message">Te Amo Gabriela<br>Todos los que amo están en ti<br>y tú en todo lo que amo.</div>

    <script>
        const messages = [
            "Todos los que amo están en ti y tú en todo lo que amo.",
            "Y si te dijeran que el sol no saldrá esta mañana, ¿les creerías?",
            "Si te contara que mi mundo se acaba, ¿me entenderías?",
            "Si te digo que te necesito, es porque sin ti estoy sufriendo.",
            "Si te dijera que no te amo, te estaría mintiendo."
        ];
        const colors = ["#ffb6c1", "#add8e6", "#dda0dd", "#f5b7b1", "#98fb98"];
        let index = 0;

        function nextScreen(event) {
            index = (index + 1) % messages.length;
            document.body.style.background = colors[index];
            document.getElementById("message").innerHTML = `Te Amo Gabriela<br>${messages[index]}`;
            createHeart(event.clientX, event.clientY);
        }

        function createHeart(x, y) {
            let heart = document.createElement("div");
            heart.innerHTML = "❤️";
            heart.className = "heart";
            heart.style.left = `${x}px`;
            heart.style.top = `${y}px`;
            document.body.appendChild(heart);
            setTimeout(() => heart.remove(), 1500);
        }
    </script>
</body>
</html>
