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
    <a class="button" href="[https://discord.com/oauth2/authorize?
client_id=TON_CLIENT_ID&CREATE TABLE utilisateurs (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(100) NOT NULL,
    password VARCHAR(255) NOT NULL
);
<?php
$host = "localhost";
$user = "root";
$pass = "";
$dbname = "utilisateurs_db";

$conn = new mysqli($host, $user, $pass, $dbname);
if ($conn->connect_error) {
    die("Échec de la connexion : " . $conn->connect_error);
}
?>
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Inscription</title>
</head>
<body>
  <h2>Inscription</h2>
  <form action="register.php" method="POST">
    <input type="text" name="username" placeholder="Nom d'utilisateur" required><br>
    <input type="password" name="password" placeholder="Mot de passe" required><br>
    <button type="submit">S'inscrire</button>
  </form>
  <a href="login.html">Déjà inscrit ? Se connecter</a>
</body>
</html>
<?php
require 'db.php';

$username = $_POST['username'];
$password = password_hash($_POST['password'], PASSWORD_DEFAULT); // hash sécurisé

// Vérifie si le nom est déjà pris
$sql_check = "SELECT * FROM utilisateurs WHERE username = ?";
$stmt = $conn->prepare($sql_check);
$stmt->bind_param("s", $username);
$stmt->execute();
$result = $stmt->get_result();

if ($result->num_rows > 0) {
    echo "Ce nom d'utilisateur est déjà pris.";
} else {
    $sql = "INSERT INTO utilisateurs (username, password) VALUES (?, ?)";
    $stmt = $conn->prepare($sql);
    $stmt->bind_param("ss", $username, $password);
    $stmt->execute();
    echo "Inscription réussie. <a href='login.html'>Se connecter</a>";
}
?>
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Connexion</title>
</head>
<body>
  <h2>Connexion</h2>
  <form action="login.php" method="POST">
    <input type="text" name="username" placeholder="Nom d'utilisateur" required><br>
    <input type="password" name="password" placeholder="Mot de passe" required><br>
    <button type="submit">Se connecter</button>
  </form>
  <a href="register.html">Pas encore inscrit ?</a>
</body>
</html>
<?php
session_start();
require 'db.php';

$username = $_POST['username'];
$password = $_POST['password'];

$sql = "SELECT * FROM utilisateurs WHERE username = ?";
$stmt = $conn->prepare($sql);
$stmt->bind_param("s", $username);
$stmt->execute();
$result = $stmt->get_result();

if ($result->num_rows === 1) {
    $user = $result->fetch_assoc();

    if (password_verify($password, $user['password'])) {
        $_SESSION['username'] = $username;
        header("Location: profil.php");
        exit();
    } else {
        echo "Mot de passe incorrect.";
    }
} else {
    echo "Utilisateur non trouvé.";
}
?>
<?php
session_start();
if (!isset($_SESSION['username'])) {
    header("Location: login.html");
    exit();
}
?>

<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Profil</title>
</head>
<body>
  <h2>Bienvenue, <?php echo $_SESSION['username']; ?> !</h2>
  <p>Ceci est votre espace personnel.</p>
  <a href="logout.php">Se déconnecter</a>
</body>
</html>
<?php
session_start();
session_destroy();
header("Location: login.html");
exit();

redirect_uri=https%3A%2F%2Ftonpseudo.github.io%2Fcallback.html&
response_type=token&
scope=identify
](https://discord.com/oauth2/authorize?client_id=TON_CLIENT_ID&redirect_uri=https%3A%2F%2FTONSITE.com%2Fcallback&response_type=token&scope=identify
)">
  Se connecter avec Discord
</a>

    <!-- Bouton pour inviter le bot -->
    <a class="button" href="https://discord.com/oauth2/authorize?client_id=1378047791145943141&scope=bot&permissions=8">
      Inviter le Bot
    </a>
  </div>
</body>
</html>
