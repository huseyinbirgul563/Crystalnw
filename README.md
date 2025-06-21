<!DOCTYPE html>
<html>
<head>
    <title>Huseyinbirgul563 Sunucu</title>
    <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #1b1b1b;
            margin: 0;
            padding: 0;
            color: white;
        }

        #popup-message {
            position: fixed;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            background-color: #3c763d;
            color: #dff0d8;
            border: 3px solid #2e562f;
            padding: 12px 20px;
            border-radius: 8px;
            font-family: 'Press Start 2P', cursive;
            font-size: 12px;
            z-index: 1000;
            display: none;
            box-shadow: 0 0 20px #0f0;
        }

        .ip-box {
            background: #2d2d2d;
            border: 4px solid #444;
            border-radius: 10px;
            padding: 20px;
            margin-top: 30px;
            font-size: 14px;
            color: #00ffff;
            font-family: 'Press Start 2P', cursive;
            cursor: pointer;
            user-select: none;
            width: fit-content;
            margin-left: auto;
            margin-right: auto;
            box-shadow: 0 0 15px #0ff;
            transition: transform 0.2s ease, box-shadow 0.2s ease;
        }

        .ip-box.active {
            transform: scale(0.95);
            box-shadow: 0 0 25px #0ff, 0 0 5px #0ff inset;
        }

        .ip-box:hover {
            background-color: #3a3a3a;
            box-shadow: 0 0 25px #0ff, 0 0 5px #0ff inset;
        }

        .social-links {
            margin-top: 30px;
        }

        .social-link {
            display: inline-flex;
            align-items: center;
            margin: 10px;
            text-decoration: none;
            color: #fff;
            font-size: 16px;
        }

        .social-link img {
            width: 40px;
            height: 40px;
            margin-right: 8px;
        }

        .social-link:hover {
            color: #0ff;
        }

        footer {
            margin-top: 60px;
            padding: 20px;
            background-color: #222;
            color: #0ff;
            font-family: 'Press Start 2P', cursive;
            font-size: 12px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
            border-top: 2px solid #0ff;
        }
    </style>
</head>
<body>

    <div id="popup-message">📋 IP Adresi Kopyalandı!</div>

    <div class="ip-box" onclick="copyIP()">
        IP: play.crystalnw.xyz
    </div>

    <h1>Hoş Geldiniz!</h1>
    <p>Bu benim Minecraft sunucumun resmi sitesidir.</p>

    <div class="social-links">
        <a class="social-link" href="https://youtube.com/@huseyinbirgul563" target="_blank">
            <img src="https://cdn-icons-png.flaticon.com/512/1384/1384060.png" alt="YouTube">
            youtube.com/@huseyinbirgul563
        </a>
        <a class="social-link" href="https://kick.com/huseyinbirgul563" target="_blank">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6e/Kick.com_logo.svg/512px-Kick.com_logo.svg.png" alt="Kick">
            kick.com/huseyinbirgul563
        </a>
    </div>

    <footer>
        <h2>Hakkımda</h2>
        <p>
            Kurucu: <strong>huseyinbirgul563</strong><br>
            Adminlar: <strong>furki1903</strong>, <strong>ccytcihangir</strong>, <strong>PMP</strong>
        </p>
    </footer>

    <script>
        function copyIP() {
            const ip = "play.crystalnw.xyz";
            navigator.clipboard.writeText(ip).then(function () {
                const popup = document.getElementById("popup-message");
                const ipBox = document.querySelector(".ip-box");

                ipBox.classList.add("active");

                popup.style.display = "block";

                setTimeout(() => {
                    ipBox.classList.remove("active");
                }, 200);

                setTimeout(() => {
                    popup.style.display = "none";
                }, 2000);
            });
        }
    </script>
</body>
</html>
