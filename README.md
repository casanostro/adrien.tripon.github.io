<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Site en chantier</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Oswald:wght@500&display=swap');

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Oswald', sans-serif;
            background: #111;
            color: #ffcc00;
            text-align: center;
            overflow: hidden;
        }

        .container {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
        }

        h1 {
            font-size: 3rem;
            text-transform: uppercase;
            letter-spacing: 3px;
            animation: flash 1.5s infinite alternate;
        }

        @keyframes flash {
            from { opacity: 1; }
            to { opacity: 0.5; }
        }

        .barriere {
            width: 100%;
            height: 50px;
            background: repeating-linear-gradient(
                45deg,
                #ffcc00,
                #ffcc00 25px,
                #111 25px,
                #111 50px
            );
            position: absolute;
            bottom: 50px;
            left: 0;
            animation: move-barriere 2s linear infinite;
        }

        @keyframes move-barriere {
            from { background-position: 0 0; }
            to { background-position: 100px 0; }
        }

        .warning {
            font-size: 1.5rem;
            margin-top: 20px;
            opacity: 0;
            transform: scale(0.5);
            animation: fadeInScale 1s forwards 2s;
        }

        @keyframes fadeInScale {
            to {
                opacity: 1;
                transform: scale(1);
            }
        }

        .spark-container {
            position: absolute;
            top: 50%;
            left: 50%;
            width: 100%;
            height: 100%;
            overflow: hidden;
            z-index: -1;
        }

        .spark {
            position: absolute;
            width: 5px;
            height: 5px;
            background: orange;
            border-radius: 50%;
            box-shadow: 0 0 10px orange;
            animation: sparks 0.5s linear infinite;
        }

        @keyframes sparks {
            from {
                transform: translateY(0);
                opacity: 1;
            }
            to {
                transform: translateY(-100px);
                opacity: 0;
            }
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>⚠️ Site en chantier ⚠️</h1>
        <p class="warning">Quelque chose de dingue arrive... Prépare-toi !</p>
    </div>

    <div class="barriere"></div>

    <div class="spark-container"></div>

    <script>
        function createSparks() {
            const container = document.querySelector('.spark-container');
            for (let i = 0; i < 20; i++) {
                let spark = document.createElement('div');
                spark.classList.add('spark');
                spark.style.left = Math.random() * window.innerWidth + 'px';
                spark.style.top = Math.random() * window.innerHeight + 'px';
                spark.style.animationDuration = (Math.random() * 1 + 0.5) + 's';
                container.appendChild(spark);

                setTimeout(() => {
                    spark.remove();
                }, 1000);
            }
        }

        setInterval(createSparks, 300);
    </script>

</body>
</html>
