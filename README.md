<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Connexion</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            height: 100vh;
            background: linear-gradient(135deg, #5865F2, #8b5cf6);
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .container {
            background: white;
            width: 350px;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            text-align: center;
        }

        h1 {
            margin-bottom: 20px;
            color: #333;
        }

        input {
            width: 100%;
            padding: 12px;
            margin: 10px 0;
            border-radius: 8px;
            border: 1px solid #ccc;
            font-size: 14px;
        }

        button {
            width: 100%;
            padding: 12px;
            margin-top: 10px;
            border-radius: 8px;
            border: none;
            font-size: 15px;
            cursor: pointer;
        }

        .login-btn {
            background: #8b5cf6;
            color: white;
        }

        .login-btn:hover {
            background: #7c3aed;
        }

        .discord-btn {
            background: #5865F2;
            color: white;
            margin-top: 15px;
        }

        .discord-btn:hover {
            background: #4752c4;
        }

        .divider {
            margin: 20px 0;
            color: #aaa;
            font-size: 14px;
        }

        footer {
            margin-top: 15px;
            font-size: 12px;
            color: #777;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Connexion</h1>

    <input type="email" placeholder="Adresse email">
    <input type="password" placeholder="Mot de passe">

    <button class="login-btn">Se connecter</button>

    <div class="divider">ou</div>

    <button class="discord-btn">
        🔗 Se connecter avec Discord
    </button>

    <footer>
        En te connectant, tu acceptes les conditions.
    </footer>
</div>

</body>
</html>
