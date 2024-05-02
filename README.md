<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minecraft: Modded for PSVita</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(to bottom, #f3f4f6, #e1e5ea);
            color: #333;
        }

        .header {
            background-color: #333;
            color: white;
            padding: 20px;
            text-align: center;
            border-bottom: 4px solid #555;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        .nav {
            background-color: #666;
            overflow: hidden;
            display: flex;
            justify-content: center;
            border-bottom: 2px solid #444;
        }

        .nav a {
            color: white;
            text-decoration: none;
            padding: 14px 20px;
            font-size: 20px;
            margin: 0 10px;
            position: relative;
            transition: background 0.3s, color 0.3s;
            z-index: 1;
            font-weight: bold;
            letter-spacing: 1px;
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

        .content {
            padding: 40px;
            text-align: center;
            display: none;
            opacity: 0;
            transition: opacity 0.5s ease-in-out;
        }

        .content.active {
            display: block;
            opacity: 1;
        }

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
            font-size: 36px;
            margin-bottom: 20px;
            color: #333;
            font-weight: bold;
        }

        p {
            font-size: 20px;
            line-height: 1.6;
            color: #555;
        }
    </style>
</head>
<body>

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
    <h2>Home</h2>
    <p>Welcome to Minecraft: Modded for PSVita. Minecraft: Modded is a modded version of Minecraft PSVita that allows you to play with normal Minecraft PSVita players. Minecraft: Modded offers various features such as custom worlds, custom textures packs, custom lobby, and much more. Please check "Updates / News" for all the details. Don't forget to join our Discord for news, updates, important announcements, and support. Thank you.</p>
</div>

<div class="content" id="updates">
    <h2>Updates / News</h2>
    <p>- Minecraft: Modded can play with normal Minecraft PSVita<br>
    - 1.20 Textures + Shaders + PVP Textures + FPS BOOST<br>
    - Custom Lobby By Mickael140810 (Chests with command blocks, all heads, all disks, elytras, tnts jumps etc etc ...)<br>
    - Custom worlds with hacked items such as Command blocks, God Stick, Creative kill potions, and even a working Hypixel Bedwars<br>
    - New Logo<br>
    - New App Design<br>
    - New Skins<br>
    - Two versions of Minecraft: Modded available: <br>
    - PVP + SHADERS + FPS BOOST<br>
    - Full Java 1.20 + Shaders<br>
    And more soon . . .</p>
</div>

<div class="content" id="download">
    <h2>Download</h2>
    <p>Minecraft: Modded is currently in development. Join Discord for more information.</p>
</div>

<div class="content" id="discord">
    <h2>Discord</h2>
    <p>Join Discord if you want to be helped for any questions or issues and for more information. <a href="https://discord.gg/ED9vNvwD8u" class="discord-link">https://discord.gg/ED9vNvwD8u</a></p>
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
</script>

</body>
</html>
