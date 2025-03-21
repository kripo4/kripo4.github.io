<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Web Visit</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }

        body {
            min-height: 100vh;
            background: url('assests/background.jpg') center/cover;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
        }

        .card {
            background: rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 30px;
            width: 90%;
            max-width: 600px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
        }

        .profile {
            display: flex;
            align-items: center;
            margin-bottom: 25px;
        }

        .avatar {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            margin-right: 20px;
            border: 3px solid white;
        }

        .info h1 {
            color: #2c3e50;
            margin-bottom: 5px;
        }

        .info p {
            color: #34495e;
            font-size: 0.9em;
        }

        .buttons {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .btn {
            padding: 12px 25px;
            border: none;
            border-radius: 50px;
            color: white;
            font-size: 16px;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            text-align: center;
            position: relative;
            overflow: hidden;
            background: linear-gradient(
                120deg,
                #4f46e5,
                #6366f1,
                #818cf8,
                #a5b4fc,
                #c7d2fe,
                #a5b4fc,
                #818cf8,
                #6366f1,
                #4f46e5
            );
            background-size: 400% 400%;
            animation: glow 8s ease-in-out infinite;
            box-shadow: 0 0 20px rgba(79,70,229,0.5);
        }

        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 200%;
            height: 100%;
            background: linear-gradient(
                120deg,
                transparent,
                rgba(255,255,255,0.15),
                transparent
            );
            transition: 0.5s;
            z-index: 1;
        }

        .btn:hover::before {
            left: 100%;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 25px rgba(99,102,241,0.8);
        }

        @keyframes glow {
            0% {
                background-position: 0% 50%;
                box-shadow: 0 0 20px rgba(79,70,229,0.5);
            }
            50% {
                background-position: 100% 50%;
                box-shadow: 0 0 40px rgba(99,102,241,0.8);
            }
            100% {
                background-position: 0% 50%;
                box-shadow: 0 0 20px rgba(79,70,229,0.5);
            }
        }

        @media (max-width: 480px) {
            .card {
                padding: 20px;
            }

            .profile {
                flex-direction: column;
                text-align: center;
            }

            .avatar {
                margin-right: 0;
                margin-bottom: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="card">
        <div class="profile">
            <img src="assests/img.jpg" class="avatar" alt="Аватар">
            <div class="info">
                <h1>nickname</h1>
                <p>Graphical Designer</p>
                <p>Cologne, Nordrhein-Westfalen, Germany</p>
            </div>
        </div>

        <div class="buttons">
            <a href="https://github.com" target="_blank" class="btn">GitHub</a>
            <a href="https://linkedin.com" target="_blank" class="btn">LinkedIn</a>
            <a href="https://example.com" target="_blank" class="btn">Example</a>
            <a href="mailto:example@mail.com" class="btn">E-Mail</a>
        </div>
    </div>
</body>
</html>