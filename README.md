<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ma Page Stylée</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f2f2f2;
            margin: 0;
            padding: 0;
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
        }

        .nav a {
            float: left;
            display: block;
            color: white;
            text-align: center;
            padding: 14px 20px;
            text-decoration: none;
            font-size: 17px;
        }

        .nav a:hover {
            background-color: #ddd;
            color: black;
        }

        .content {
            padding: 20px;
        }
    </style>
</head>
<body>

<div class="header">
    <h1>Ma Page Stylée</h1>
</div>

<div class="nav">
    <a href="#" class="active">Home</a>
    <a href="#">Menu</a>
    <a href="#">Mod</a>
</div>

<div class="content">
    <h2>Contenu de la Page</h2>
    <p>Ceci est un exemple de page HTML avec une interface stylée.</p>
</div>

</body>
</html>
