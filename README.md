<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Erreur 404 - Construction en cours</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@700&display=swap');

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Orbitron', sans-serif;
            background: #0a0a0a;
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
            color: #ff4500;
            text-shadow: 0 0 10px #ff4500, 0 0 20px #ff2200;
            animation: blink 1.5s infinite alternate;
        }

        @keyframes blink {
            from { opacity: 1; }
            to { opacity: 0.5; }
        }

        .subtext {
            font-size: 1.5rem;
            margin-top: 20px;
            color: #ffcc00;
        }

        .factory {
            position: absolute;
            width: 100%;
            height: 100vh;
            background: url('https://source.unsplash.com/1600x900/?industrial,cyberpunk') no-repeat center center/cover;
            opacity: 0.3;
            filter: blur(3px);
        }

        .crane {
            position: absolute;
            width: 100px;
            height: 100px;
            top: 10%;
            left: 10%;
            animation: move-crane 4s infinite alternate ease-in-out;
        }

        @keyframes move-crane {
            from { transform: translateY(0); }
            to { transform: translateY(30px); }
        }

        .lights {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle, rgba(255,140,0,0.2) 10%, rgba(0,0,0,0) 80%);
            pointer-events: none;
            animation: flicker 2s infinite alternate;
        }

        @keyframes flicker {
            from { opacity: 0.8; }
            to { opacity: 0.5; }
        }

        .sparks-container {
            position: absolute;
            top: 50%;
            left: 50%;
            width: 100%;
            height: 100%;
            overflow: hidden;
            z-index: 2;
        }

        .spark {
            position: absolute;
            width: 5px;
            height: 5px;
            background: orange;
            border-radius: 50%;
            box-shadow: 0 0 10px orange;
            animation: sparks 0.8s linear infinite;
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
    </style

