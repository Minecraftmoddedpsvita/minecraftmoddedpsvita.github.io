<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minecraft Modded for PSVita</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f2f2f2;
            color: #333;
        }

        .header {
            background-color: #333;
            color: white;
            padding: 20px;
            text-align: center;
        }

        .nav {
            background-color: #666;
            overflow: hidden;
            display: flex;
            justify-content: center;
        }

        .nav a {
            color: white;
            text-decoration: none;
            padding: 14px 20px;
            font-size: 17px;
            margin: 0 10px;
            position: relative;
            transition: color 0.3s, background-color 0.3s;
        }

        .nav a:hover {
            background-color: #000;
            color: #fff;
        }

        .nav a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 50%;
            width: 0;
            height: 2px;
            background-color: #fff;
            transition: width 0.3s ease, left 0.3s ease;
        }

        .nav a:hover::after,
        .nav a.active::after {
            width: 100%;
            left: 0;
        }

        .content {
            padding: 20px;
            text-align: center;
        }

        .download {
            display: none;
        }

        .download.show {
            display: block;
            animation: fadeIn 0.5s;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }
    </style>
</head>
<body>

<div class="header">
    <h1>Minecraft Modded for PSVita</h1>
</div>

<div class="nav">
    <a href="#" class="active" onclick="showTab('home')">Home</a>
    <a href="#" onclick="showTab('menu')">Menu</a>
    <a href="#" onclick="showTab('download')">Download</a>
    <a href="#" onclick="showTab('discord')">Discord</a>
</div>

<div class="content" id="home">
    <h2>Welcome to Minecraft Modded for PSVita</h2>
    <p>This is the homepage content. Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
</div>

<div class="content" id="menu">
    <h2>Menu</h2>
    <p><strong>What's new?</strong><br>
    - Custom Mini-games Lobby made by Mickael140810<br>
    - Custom 1.20 textures packs + shaders made by Mickael140810<br>
    - New custom skins<br>
    - Custom worlds with NBTs and Hypixel Bedwars<br>
    - New App design<br>
    - Larger worlds and max players are in the list but not sure of doing it<br>
    - Custom HUD Menu<br>
    - And More ...<br><br>
    Join Discord for newest information.</p>
</div>

<div class="content download" id="download">
    <h2>Download</h2>
    <p>Download Minecraft Modded for PSVita here.</p>
</div>

<div class="content" id="discord">
    <h2>Discord</h2>
    <p>Join our Discord server for support and discussions <a href="https://discord.gg/ED9vNvwD8u">https://discord.gg/ED9vNvwD8u</a>.</p>
</div>

<script>
    function showTab(tabName) {
        var i;
        var content = document.getElementsByClassName("content");
        for (i = 0; i < content.length; i++) {
            content[i].style.display = "none";
        }
        document.getElementById(tabName).style.display = "block";
    }
</script>

</body>
</html>
