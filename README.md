<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minecraft: Modded for PSVita</title>
    <style>
        /* Styles communs pour toutes les tailles d'écran */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(to bottom, #f3f4f6, #e1e5ea);
            color: #333;
            overflow-x: hidden;
            animation: gradientAnimation 10s infinite alternate;
        }

        /* Animation du fond */
        @keyframes gradientAnimation {
            0% { background: linear-gradient(to bottom, #f3f4f6, #e1e5ea); }
            100% { background: linear-gradient(to bottom, #e1e5ea, #f3f4f6); }
        }

        /* Styles pour les écrans larges (PC) */
        .desktop .nav {
            display: flex;
            justify-content: center;
            margin: 20px;
        }

        .desktop .content {
            display: inline-block;
            width: calc(20% - 40px);
            margin: 20px;
            vertical-align: top;
        }

        /* Styles pour les appareils mobiles */
        .mobile .nav {
            display: block;
            text-align: center;
            margin-bottom: 20px;
        }

        .mobile .nav a {
            display: block;
            padding: 10px;
            margin: 5px auto;
            border-radius: 5px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* Ajout d'une ombre */
        }

        .mobile .content {
            display: block;
            width: 80%;
            margin: 0 auto;
            margin-bottom: 20px;
        }

        /* Styles communs pour les onglets */
        .nav a {
            color: white;
            text-decoration: none;
            padding: 14px 20px;
            font-size: 18px;
            margin: 0 10px;
            position: relative;
            transition: background 0.3s, color 0.3s;
            z-index: 1;
            font-weight: bold;
            letter-spacing: 1px;
            border-radius: 5px;
        }

        .nav a:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to bottom, rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.5));
            z-index: -1;
            opacity: 0;
            transition: opacity 0.3s;
            border-radius: 5px;
        }

        .nav a:hover:before {
            opacity: 1;
        }

        .nav a:hover {
            color: transparent;
        }

        .nav a:hover::after {
            content: attr(data-text);
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 2;
            color: white;
        }

        /* Styles pour le contenu */
        .content {
            padding: 20px;
            text-align: center;
            opacity: 0;
            transition: opacity 0.5s ease-in-out;
            border-radius: 10px;
            background-color: #fff;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .content.active {
            opacity: 1;
        }

        /* Autres styles */
        .gradient-hover {
            background: linear-gradient(90deg, #ff7e5f, #feb47b);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            transition: background-position 0.5s;
            position: relative;
        }

        .gradient-hover:hover {
            background-position: 100% 0;
        }

        .discord-link {
            color: #007bff;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s;
        }

        .discord-link:hover {
            color: #0056b3;
        }

        h2 {
            font-size: 26px;
            margin-bottom: 20px;
            color: #333;
            font-weight: bold;
        }

        p {
            font-size: 16px;
            line-height: 1.6;
            color: #555;
        }

        .btn {
            display: inline-block;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            text-decoration: none;
            transition: background-color 0.3s;
            padding: 10px 20px;
            margin-top: 20px;
        }

        .btn:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body class="desktop">
<div class="header">
    <h1>Minecraft: Modded for PSVita</h1>
</div>

<div class="nav">
    <a href="#" class="gradient-hover" data-text="Home" onclick="showTab('home')">Home</a>
    <a href="#" class="gradient-hover" data-text="Updates / News" onclick="showTab('updates')">Updates / News</a>
    <a href="#" class="gradient-hover" data-text="Download" onclick="showTab('download')">Download</a>
    <a href="#" class="gradient-hover" data-text="Discord" onclick="showTab('discord')">Discord</a>
    <a href="#" class="gradient-hover" data-text="Credit" onclick="showTab('credit')">Credit</a>
</div>

<div class="content active" id="home">
    <h2>Welcome to Minecraft: Modded for PSVita</h2>
    <p>Minecraft: Modded is a modded version of Minecraft PSVita that brings exciting new features and enhancements. Join our community and experience Minecraft like never before!</p>
    <a href="#" class="btn gradient-hover" onclick="showTab('download')">Download Now</a>
</div>

<div class="content" id="updates">
    <h2>Updates / News</h2>
    <p>- Minecraft: Modded can now play with normal Minecraft PSVita.</p>
    <p>- Includes 1.20 Textures + Shaders + PVP Textures + FPS BOOST.</p>
    <p>- Custom Lobby By Mickael140810 (Chests with command blocks, all heads, all disks, elytras, tnts jumps etc etc ...).</p>
    <p>- Custom worlds with hacked items such as Command blocks, God Stick, Creative kill potions, and even a working Hypixel Bedwars.</p>
    <p>- New Logo, App Design, and Skins.</p>
    <p>- Two versions of Minecraft: Modded available: PVP + SHADERS + FPS BOOST and Full Java 1.20 + Shaders.</p>
    <p>- And more updates coming soon...</p>
</div>

<div class="content" id="download">
    <h2>Download</h2>
    <p>Minecraft: Modded is currently in development. Join our Discord server for more information and updates.</p>
    <a href="https://discord.gg/ED9vNvwD8u" class="btn gradient-hover" target="_blank">Join Discord</a>
</div>

<div class="content" id="discord">
    <h2>Discord</h2>
    <p>Join our Discord server to connect with the community, get help, and stay updated with the latest news and announcements.</p>
    <a href="https://discord.gg/ED9vNvwD8u" class="btn gradient-hover" target="_blank">Join Discord</a>
</div>

<div class="content" id="credit">
    <h2>Credit</h2>
    <p>Made by Mickael140810 alias Mickado. Minecraft: Modded's logo made by Matt19220. Skins made with the help of Aquamarine.</p>
</div>

<script>
    function showTab(tabName) {
        var i, tabContent, tabLinks;
        tabContent = document.getElementsByClassName("content");
        for (i = 0; i < tabContent.length; i++) {
            tabContent[i].classList.remove('active');
        }
        document.getElementById(tabName).classList.add('active');
    }

    // Détecter le type d'appareil et changer le comportement en conséquence
    if (/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
        document.body.classList.remove("desktop");
        document.body.classList.add("mobile");
    }
</script>

</body>
</html>
