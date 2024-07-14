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
    <p><strong>MINECRAFT: MODDED V1 [RELEASE]</strong></p>
    <p>Here is what new about Modded V1:</p>
    <ul>
        <li>Custom Skin Packs (35+)</li>
        <li>5 New Glide Maps (not made by modded community)</li>
        <li>New PSN Status changed to "(username Play Minecraft: Modded V1"</li>
        <li>PC / PS3 Worlds Converted to PSVita Worlds such as skywars, skyblock, bedwars, hunger games etc . . . (fully working)</li>
        <li>New texture pack</li>
        <li>Custom name with the color that you want. (create a ticket on the discord to apply.)</li>
        <li>New UI, New Background</li>
        <li>Custom Mini-Games Lobby</li>
        <li>All DLCs unlocked</li>
        <li>New 1.21 Dog Texture "Woods Wolf".</li>
        <li>Increased lights</li>
        <li>New buttons called "Updates & Options" and "Modded Updates" to check what's new when you update</li>
        <li>PS3/PS4 BUTTON TEXTURES</li>
        <li>There will be a lot of new updates to fix bugs, to add news things etc . . . Stay tuned on the discord and the website.</li>
    </ul>
    <p>All the download links and instructions are in the discord and the website.</p>
</div>

<div class="content" id="download">
    <h2>Minecraft: Modded V1 PSVita Released.</h2>
    <a href="https://discord.gg/ED9vNvwD8u" class="btn gradient-hover" target="_blank">Download Here</a>
    <p>Size: 18.14MB</p>
    <p>Official Discord: <a href="https://discord.gg/ED9vNvwD8u" class="discord-link" target="_blank">https://discord.gg/ED9vNvwD8u</a></p>
</div>

<div class="content" id="discord">
    <h2>Discord</h2>
    <p>Join our Discord server to connect with the community, get help, and stay updated with the latest news and announcements.</p>
    <a href="https://discord.gg/Edeee2nsvb" class="btn gradient-hover" target="_blank">Join Discord</a>
    <p>Rejoignez notre Discord: <a href="https://discord.gg/Edeee2nsvb" class="discord-link" target="_blank">https://discord.gg/Edeee2nsvb</a></p>
</div>

<div class="content" id="credit">
    <h2>Credit</h2>
    <p>Special thanks to the following contributors who made this mod possible:</p>
    <ul>
        <li>Lead Developer: John Doe</li>
        <li>Graphic Designer: Jane Smith</li>
        <li>Community Manager: Alex Johnson</li>
        <li>Tester: Emily Davis</li>
    </ul>
</div>

<div class="content" id="faq">
    <h2>FAQ</h2>
    <div class="faq-item" onclick="toggleFaq(this)">
        <h3>What is Minecraft: Modded for PSVita?</h3>
        <div class="faq-answer">
            <p>Minecraft: Modded for PSVita is a customized version of Minecraft for the PlayStation Vita, featuring new skins, maps, textures, and various enhancements.</p>
        </div>
    </div>
    <div class="faq-item" onclick="toggleFaq(this)">
        <h3>How do I install the mod?</h3>
        <div class="faq-answer">
            <p>You can find installation instructions and download links on our Discord server and website.</p>
        </div>
    </div>
    <div class="faq-item" onclick="toggleFaq(this)">
        <h3>Is this mod free?</h3>
        <div class="faq-answer">
            <p>Yes, Minecraft: Modded for PSVita is free to download and use.</p>
        </div>
    </div>
    <div class="faq-item" onclick="toggleFaq(this)">
        <h3>Where can I report bugs or suggest new features?</h3>
        <div class="faq-answer">
            <p>You can report bugs or suggest new features on our Discord server.</p>
        </div>
    </div>
</div>

<script>
    function showTab(tabId) {
        var tabs = document.querySelectorAll('.content');
        tabs.forEach(function (tab) {
            tab.classList.remove('active');
        });
        document.getElementById(tabId).classList.add('active');
    }

    function toggleFaq(faqItem) {
        var answer = faqItem.querySelector('.faq-answer');
        if (answer.style.display === 'block') {
            answer.style.display = 'none';
        } else {
            answer.style.display = 'block';
        }
    }
</script>

</body>
</html>
