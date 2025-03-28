<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Adrien | CV Brutaliste</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Oswald:wght@300;700&display=swap');
 
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
 
        body {
            font-family: 'Oswald', sans-serif;
            background: #121212;
            color: #e0e0e0;
            text-transform: uppercase;
        }
 
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px;
            background: #1a1a1a;
            border-bottom: 3px solid #e0e0e0;
        }
 
        h1 {
            font-size: 2rem;
            letter-spacing: 2px;
        }
 
        nav ul {
            list-style: none;
            display: flex;
        }
 
        nav ul li {
            margin: 0 15px;
        }
 
        nav ul li a {
            text-decoration: none;
            color: #e0e0e0;
            font-size: 1.2rem;
            transition: 0.3s;
        }
 
        nav ul li a:hover {
            color: #ff0033;
        }
 
        .section {
            padding: 50px 10%;
            border-bottom: 2px solid #333;
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease-in-out;
        }
 
        .section.show {
            opacity: 1;
            transform: translateY(0);
        }
 
        h2 {
            font-size: 2rem;
            border-bottom: 3px solid #e0e0e0;
            display: inline-block;
            padding-bottom: 5px;
            margin-bottom: 20px;
        }
 
        .exp-card {
            background: #1a1a1a;
            padding: 20px;
            margin: 15px 0;
            border-left: 5px solid #ff0033;
        }
 
        ul {
            list-style: square;
            padding-left: 20px;
        }
 
        footer {
            text-align: center;
            padding: 20px;
            background: #1a1a1a;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Adrien</h1>
        <nav>
            <ul>
                <li><a href="#profil">Profil</a></li>
                <li><a href="#experience">Expérience</a></li>
                <li><a href="#competences">Compétences</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>
 
    <section id="profil" class="section">
        <h2>Profil</h2>
        <p>Chef de projet supply chain & méthodes, passionné par l’optimisation des flux et la stratégie industrielle.</p>
    </section>
 
    <section id="experience" class="section">
        <h2>Expérience</h2>
        <div class="exp-card">
            <h3>Samsung</h3>
            <p>Optimisation des processus d’automatisation des flux de commandes et affinement des KPI.</p>
        </div>
        <div class="exp-card">
            <h3>Autres Expériences</h3>
            <p>Responsable méthodes et processus dans divers environnements industriels.</p>
        </div>
    </section>
 
    <section id="competences" class="section">
        <h2>Compétences</h2>
        <ul>
            <li>Gestion de projets supply chain</li>
            <li>Optimisation des processus</li>
            <li>Automatisation (VBA, Power Query, SAP)</li>
        </ul>
    </section>
 
    <section id="contact" class="section">
        <h2>Contact</h2>
        <p>Email : <a href="mailto:adrien@example.com">adrien@example.com</a></p>
        
LinkedIn : <a href="https://www.linkedin.com/in/adrien-tripon" target="_blank">Mon profil</a></p>
    </section>
 
    <footer>
        <p>© 2025 Adrien Tripon | Tous droits réservés.</p>
    </footer>
 
    <script>
        document.addEventListener("DOMContentLoaded", function () {
            const sections = document.querySelectorAll(".section");
 
            const revealSection = () => {
                sections.forEach((section) => {
                    const sectionTop = section.getBoundingClientRect().top;
                    if (sectionTop < window.innerHeight * 0.85) {
                        section.classList.add("show");
                    }
                });
            };
 
            window.addEventListener("scroll", revealSection);
            revealSection();
        });
    </script>
</body>
</html>
 
