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
            overflow-x: hidden;
            animation: gradientAnimation 10s infinite alternate;
        }

        @keyframes gradientAnimation {
            0% { background: linear-gradient(to bottom, #f3f4f6, #e1e5ea); }
            100% { background: linear-gradient(to bottom, #e1e5ea, #f3f4f6); }
        }

        .header {
            background-color: #333;
            color: white;
            padding: 20px;
            text-align: center;
            border-bottom: 4px solid #555;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            animation: fadeIn 1s;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .nav {
            background-color: #666;
            overflow: hidden;
            display: flex;
            justify-content: center;
            border-bottom: 2px solid #444;
            border-radius: 10px;
            margin: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            animation: fadeInDown 1s;
        }

        @keyframes fadeInDown {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
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

        .content {
            padding: 40px;
            text-align: center;
            display: none;
            opacity: 0;
            transition: opacity 0.5s ease-in-out;
            border-radius: 10px;
            background-color: #fff;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            margin-top: 20px;
            animation: fadeInContent 0.5s;
        }

        @keyframes fadeInContent {
            from { opacity: 0; }
            to { opacity: 1; }
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

        .btn {
            display: inline-block;
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            font-size: 18px;
            text-decoration: none;
            transition: background-color 0.3s;
            margin-top: 20px;
        }

        .btn:hover {
            background-color: #0056b3;
        }

        .faq-item {
            margin-bottom: 20px;
            cursor: pointer;
        }

        .faq-item h3 {
            font-size: 24px;
            margin: 0;
            color: #007bff;
            transition: color 0.3s;
        }

        .faq-item:hover h3 {
            color: #0056b3;
        }

        .faq-answer {
            display: none;
            font-size: 18px;
            color: #555;
            margin-top: 10px;
            padding-left: 20px;
            border-left: 3px solid #007bff;
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
    <a href="#" class="gradient-hover" data-text="FAQ" onclick="showTab('faq')">FAQ</a>
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
    <h2>MINECRAFT: MODDED V1 IS NOT RELEASED YET, THOSES INSTRUCTIONS ARE FOR THE FUTURE !!!</h2>
    <a href="https://discord.gg/ED9vNvwD8u" class="btn gradient-hover" target="_blank">Join Discord</a>
    <h2>Minecraft: Modded V1 RELEASE</h2>
    <p>Tutorial how to install Minecraft: Modded V1.</p>
    <p>
        <strong>1st step:</strong> Check your region code of the Minecraft you're currently using. If it is USA, or Japan, you can install Minecraft: Modded V1 without uninstalling Minecraft. If your Minecraft region code is Europe (PCSB00560), you will have to uninstall your Minecraft because Minecraft: Modded V1 is currently only on Europe. (USA AND JAPAN RELEASE SOON . . .)
    </p>
    <p><strong>2nd step:</strong> Download the "Minecraft_ModdedV1_Install_Folder" folder. Download "Minecraft_Modded_reFiles" folder, and download "Minecraft_ModdedV1_Custom_Worlds </p>
    <p><strong>3rd step:</strong> Slide the "Minecraft_ModdedV1_Install_Folder" , "Minecraft_Modded_reFiles" and "Minecraft_ModdedV1_Custom_Worlds to your PSVita.</p>
    <p><strong>4th step:</strong> Go on "Minecraft_ModdedV1_Install_Folder", press triangle, go to "More" and choose "Install Folder".</p>
    <p><strong>5th step:</strong> Open "Minecraft_Modded_reFiles" folder and slide the "reAddcount" and the "rePatch" folder to ux0.</p>
     <p><strong>6th step:</strong> Open "Minecraft_ModdedV1_Custom_Worlds" copy the "savegames" folder, go to ux0:/data and paste.</p>
    <p><strong>7th step:</strong> Launch Minecraft: Modded V1 for few seconds then close it.</p>
    <p><strong>8th step:</strong> Launch "Save Manager" app, tap on "Minecraft: Modded V1", tap on ***RESTORE*** then tap on "SLOT9", then press X. (this step will allow you to have the custom worlds.)</p>
    <p><strong>9th step:</strong> Launch Minecraft: Modded V1, and enjoy!</p>
</div>

<div class="content" id="discord">
    <h2>Discord</h2>
    <p>Join our Discord server to connect with the community, get help, and stay updated with the latest news and announcements.</p>
    <a href="https://discord.gg/ED9vNvwD8u" class="btn gradient-hover" target="_blank">Join Discord</a>
</div>

<div class="content" id="credit">
    <h2>Credit</h2>
    <p>Made by Mickael140810 alias Mickado. Minecraft: Modded's logo made by Matt19220. Special Thanks to: SkyForces, PhoenixArc, Matt19220, Zealous Chuck, Haasman, Lee</p>
</div>

<div class="content" id="faq">
    <h2>FAQ</h2>
    <div class="faq-item" onclick="toggleFaqAnswer('faq1')">
        <h3>Can I have Minecraft: Enhanced and Minecraft: Modded at the same time?</h3>
        <div class="faq-answer" id="faq1">
            <p>Yes, of course! Just install Minecraft: Enhanced USA or JPN Edition, and keep Minecraft: Modded to Europe edition (PSCB00560).</p>
        </div>
    </div>
    <div class="faq-item" onclick="toggleFaqAnswer('faq2')">
        <h3>Can I have normal Minecraft and Minecraft: Modded V1 ?</h3>
        <div class="faq-answer" id="faq2">
            <p>Yes, of course! Just make sure your normal Minecraft is JAPAN or USA edition, and keep Minecraft: Modded V1 Europe edition (PCSB00560).</p>
        </div>
    </div>
</div>

<script>
    function showTab(tabName) {
        var i, tabContent;
        tabContent = document.getElementsByClassName("content");
        for (i = 0; i < tabContent.length; i++) {
            tabContent[i].classList.remove('active');
        }
        document.getElementById(tabName).classList.add('active');
        window.scrollTo(0, 0); // scroll to top when tab changes
    }

    function toggleFaqAnswer(faqId) {
        var answer = document.getElementById(faqId);
        if (answer.style.display === "none" || answer.style.display === "") {
            answer.style.display = "block";
        } else {
            answer.style.display = "none";
        }
    }
</script>

</body>
</html>
