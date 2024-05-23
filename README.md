# Xenom-football

<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Site de Football</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #e9e9e9;
            color: #333;
        }
        header {
            background-color: #444;
            color: #fff;
            padding: 20px 0;
            text-align: center;
        }
        nav {
            background-color: #555;
            overflow: hidden;
        }
        nav a {
            float: left;
            display: block;
            color: white;
            text-align: center;
            padding: 14px 16px;
            text-decoration: none;
        }
        nav a:hover {
            background-color: #777;
            color: white;
        }
        .container {
            width: 80%;
            margin: auto;
            overflow: hidden;
        }
        .content {
            background: #fff;
            padding: 20px;
            margin-top: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h2 {
            color: #444;
        }
        footer {
            background-color: #444;
            color: #fff;
            text-align: center;
            padding: 10px 0;
            margin-top: 20px;
        }
        .carousel {
            position: relative;
            width: 100%;
            overflow: hidden;
        }
        .carousel img {
            width: 100%;
            display: block;
        }
        .carousel-content {
            position: absolute;
            bottom: 0;
            background: rgba(0, 0, 0, 0.5);
            color: #fff;
            width: 100%;
            text-align: center;
            padding: 10px 0;
        }
        .card {
            float: left;
            width: 30%;
            margin: 1.66%;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .card img {
            width: 100%;
        }
        .card-content {
            padding: 20px;
        }
        .chart-container {
            width: 100%;
            height: 400px;
        }
    </style>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body>
    <header>
        <div class="container">
            <h1>Bienvenue sur le site de Football</h1>
        </div>
    </header>
    <nav>
        <div class="container">
            <a href="#actualites">Actualités</a>
            <a href="#competitions">Compétitions</a>
            <a href="#equipes">Équipes</a>
            <a href="#joueurs">Joueurs</a>
            <a href="#statistiques">Statistiques</a>
            <a href="#contact">Contact</a>
        </div>
    </nav>
    <div class="container">
        <div id="actualites" class="content">
            <h2>Actualités</h2>
            <div class="carousel">
                <img src="https://via.placeholder.com/800x400" alt="Actualité 1">
                <div class="carousel-content">
                    <h3>Dernière nouvelle du football</h3>
                    <p>Description de l'actualité.</p>
                </div>
            </div>
        </div>
        <div id="competitions" class="content">
            <h2>Compétitions</h2>
            <table border="1" cellpadding="10" cellspacing="0" width="100%">
                <tr>
                    <th>Compétition</th>
                    <th>Équipe A</th>
                    <th>Équipe B</th>
                    <th>Date</th>
                </tr>
                <tr>
                    <td>Championnat</td>
                    <td>Équipe 1</td>
                    <td>Équipe 2</td>
                    <td>01/06/2024</td>
                </tr>
                <tr>
                    <td>Coupe</td>
                    <td>Équipe 3</td>
                    <td>Équipe 4</td>
                    <td>05/06/2024</td>
                </tr>
            </table>
        </div>
        <div id="equipes" class="content">
            <h2>Équipes</h2>
            <div class="card">
                <img src="https://via.placeholder.com/300x200" alt="Équipe 1">
                <div class="card-content">
                    <h3>Équipe 1</h3>
                    <p>Description de l'équipe.</p>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/300x200" alt="Équipe 2">
                <div class="card-content">
                    <h3>Équipe 2</h3>
                    <p>Description de l'équipe.</p>
                </div>
            </div>
        </div>
        <div id="joueurs" class="content">
            <h2>Joueurs</h2>
            <div class="card">
                <img src="https://via.placeholder.com/300x200" alt="Joueur 1">
                <div class="card-content">
                    <h3>Joueur 1</h3>
                    <p>Description du joueur.</p>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/300x200" alt="Joueur 2">
                <div class="card-content">
                    <h3>Joueur 2</h3>
                    <p>Description du joueur.</p>
                </div>
            </div>
        </div>
        <div id="statistiques" class="content">
            <h2>Statistiques</h2>
            <div class="chart-container">
                <canvas id="statsChart"></canvas>
            </div>
            <script>
                var ctx = document.getElementById('statsChart').getContext('2d');
                var chart = new Chart(ctx, {
                    type: 'line',
                    data: {
                        labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul'],
                        datasets: [{
                            label: 'Performances des équipes',
                            backgroundColor: 'rgba(0, 119, 204, 0.3)',
                            borderColor: '#0077cc',
                            data: [10, 20, 30, 40, 50, 60, 70]
                        }]
                    },
                    options: {}
                });
            </script>
        </div>
        <div id="contact" class="content">
            <h2>Contact</h2>
            <form action="mailto:example@example.com" method="post" enctype="text/plain">
                <label for="name">Nom:</label><br>
                <input type="text" id="name" name="name"><br>
                <label for="email">Email:</label><br>
                <input type="email" id="email" name="email"><br>
                <label for="message">Message:</label><br>
                <textarea id="message" name="message" rows="4" cols="50"></textarea><br><br>
                <input type="submit" value="Envoyer">
            </form>
        </div>
    </div>
    <footer>
        <div class="container">
            <p>&copy; 2024 Site de Football. Tous droits réservés.</p>
        </div>
    </footer>
</body>
</html>
