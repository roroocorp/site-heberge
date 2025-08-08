<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Mon Bot Discord</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #7289da, #99aab5);
      color: #ffffff;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
    }

    .container {
      background-color: rgba(0, 0, 0, 0.4);
      padding: 40px;
      border-radius: 15px;
      box-shadow: 0 4px 20px rgba(0,0,0,0.3);
      max-width: 500px;
    }

    h1 {
      font-size: 32px;
      margin-bottom: 20px;
    }

    p {
      font-size: 18px;
      margin-bottom: 30px;
    }

    .button {
      display: inline-block;
      background-color: #5865F2;
      color: white;
      padding: 15px 25px;
      border-radius: 8px;
      text-decoration: none;
      font-size: 18px;
      margin: 10px;
      transition: background-color 0.3s ease;
    }

    .button:hover {
      background-color: #4752c4;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Bienvenue sur le site de mon Bot Discord</h1>
    <p>Connectez-vous avec votre compte Discord pour accéder à vos fonctionnalités personnalisées.</p>
    <p><strong>On peut ajouter le bot sur le serveur.</strong></p>

    <!-- Bouton de connexion -->
    <a class="button" href="https://discord.com/oauth2/authorize?client_id=TON_CLIENT_ID&redirect_uri=TON_REDIRECT_URI&response_type=token&scope=identify">
      Se connecter avec Discord
    </a>

    <!-- Bouton pour inviter le bot -->
    <a class="button" href="https://discord.com/oauth2/authorize?client_id=1378047791145943141&scope=bot&permissions=8">
      Inviter le Bot
    </a>
  </div>
</body>
</html>
