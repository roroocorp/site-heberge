<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Mon Tableau de Bord</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: #f4f6f8;
      color: #333;
    }

    .dashboard-container {
      padding: 20px;
      max-width: 1200px;
      margin: 0 auto;
    }

    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 30px;
    }

    header h1 {
      font-size: 2.5rem;
      color: #222;
    }

    header button {
      padding: 10px 20px;
      background-color: #ff5c5c;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: background 0.3s ease;
    }

    header button:hover {
      background-color: #e04848;
    }

    .dashboard-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
    }

    .card {
      background-color: white;
      padding: 20px;
      border-radius: 16px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.05);
    }

    .user-info {
      display: flex;
      align-items: center;
      gap: 15px;
    }

    .user-icon {
      width: 60px;
      height: 60px;
      background-color: #d8d8d8;
      border-radius: 50%;
    }

    .card h2 {
      margin: 0;
    }

    .card h3 {
      margin-top: 0;
      margin-bottom: 15px;
      color: #444;
    }

    .stats-list {
      list-style: none;
      padding: 0;
      margin: 0;
    }

    .stats-list li {
      margin-bottom: 8px;
    }

    .action-btn {
      display: block;
      width: 100%;
      padding: 12px;
      background-color: #5568fe;
      color: white;
      border: none;
      border-radius: 8px;
      margin-top: 10px;
      cursor: pointer;
      transition: background 0.3s ease;
    }

    .action-btn:hover {
      background-color: #4352e0;
    }

    .text-gray {
      color: #777;
    }
  </style>
</head>
<body>

  <div class="dashboard-container">
    <header>
      <h1>Mon Tableau de Bord</h1>
      <button>Se déconnecter</button>
    </header>

    <section class="dashboard-grid">
      <div class="card">
        <div class="user-info">
          <div class="user-icon"></div>
          <div>
            <h2>Nom d'utilisateur</h2>
            <p class="text-gray">@pseudo</p>
          </div>
        </div>
      </div>

      <div class="card">
        <h3>Statistiques</h3>
        <ul class="stats-list">
          <li>XP : 1245</li>
          <li>Niveau : 12</li>
          <li>Quêtes accomplies : 47</li>
        </ul>
      </div>

      <div class="card">
        <h3>Actions rapides</h3>
        <button class="action-btn">Voir l'inventaire</button>
        <button class="action-btn">Commencer une quête</button>
      </div>
    </section>
  </div>

</body>
</html>
