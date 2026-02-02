[LAB] Appliquer des filtres aux requêtes SQL
📝 Description du projet
Dans ce projet, j'illustre comment renforcer la sécurité d'un système en utilisant SQL pour enquêter sur des incidents potentiels. Mon rôle consiste à extraire des données précises depuis les tables de logs et d'employés afin d'identifier des tentatives de connexion suspectes et de cibler les machines nécessitant des mises à jour de sécurité critiques.

🛠️ Compétences et Outils
Langage : SQL

Concepts : Filtrage de données, Opérateurs logiques (AND, OR, NOT), Pattern matching (LIKE).

Contexte : Analyse de logs de connexion et gestion d'inventaire informatique (IAM).

🚀 Réalisation pas à pas
1. Identifier les tentatives de connexion hors horaires Cette requête récupère toutes les tentatives de connexion ayant échoué après 18h (heure de fermeture de l'entreprise) dans la table log_in_attempts. Cela permet de détecter des activités anormales durant la nuit. <img src="https://asanogo919-lab.github.io/Abdoulaye-Sanogo/img/1.png" style="width:600" >

2. Filtrer les connexions sur des dates spécifiques Pour isoler un incident survenu sur une période précise, j'utilise cette requête qui extrait toutes les tentatives de connexion ayant eu lieu les 08 et 09 mai 2025. <img src="https://asanogo919-lab.github.io/Abdoulaye-Sanogo/img/2.png" style="width:600" >

3. Exclure les zones géographiques sûres (Mexique) L'équipe ayant déterminé que l'activité suspecte ne provenait pas du Mexique, j'ai filtré les résultats pour exclure ce pays.

Méthode : Utilisation de NOT combiné à LIKE avec le pattern MEX%.

Justification : Le signe % permet de capturer à la fois les entrées "MEX" et "MEXICO" présentes dans la base de données.

<img src="https://asanogo919-lab.github.io/Abdoulaye-Sanogo/img/3.png" style="width:600" >

4. Cibler les employés du Marketing (Bâtiment Est) Pour une mise à jour matérielle ciblée, je filtre la table employees pour identifier uniquement le personnel du département Marketing situé dans le bâtiment Est. <img src="https://asanogo919-lab.github.io/Abdoulaye-Sanogo/img/4.png" style="width:600" >

5. Identifier les départements Ventes ou Finances Ici, j'utilise l'opérateur OR pour extraire la liste des employés appartenant soit au département "Sales", soit au département "Finance", afin d'appliquer un correctif de sécurité spécifique. <img src="https://asanogo919-lab.github.io/Abdoulaye-Sanogo/img/5.png" style="width:600" >

6. Isoler les employés hors département informatique Les techniciens IT ayant déjà été mis à jour, cette requête utilise WHERE NOT pour lister tous les autres employés de l'organisation qui attendent encore leur mise à jour de sécurité. <img src="https://asanogo919-lab.github.io/Abdoulaye-Sanogo/img/6.png" style="width:600" >

🎯 Résumé
Ce projet démontre ma capacité à manipuler des bases de données relationnelles pour répondre à des besoins de cybersécurité concrets. En maîtrisant les opérateurs de filtrage SQL, je suis capable d'isoler rapidement des menaces potentielles ou de segmenter des parcs informatiques pour des opérations de maintenance.
