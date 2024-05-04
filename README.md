<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minecraft: Modded for PSVita</title>
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
</script>

</body>
</html>
