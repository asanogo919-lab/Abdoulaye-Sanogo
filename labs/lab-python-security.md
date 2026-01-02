# [LAB] Algorithme de mise à jour de fichiers en Python

### 📝 Description du projet
Dans ce projet je vais développer un algorithme qui analyse un fichier contenant des adresses ip autorise à accéder à du contenu restreint et supprimer les adresses qui n'ont plus accès
Python peut automatiser ce processus 

### 🛠️ Compétences et Outils
- **Langage :** Python
- **Concepts :** Gestion de fichiers (I/O), Listes, Boucles, String parsing.
- **Contexte :** Gestion des accès (IAM) et conformité.

### 🚀 Réalisation pas à pas

**Ouvrez le fichier contenant la liste d'autorisation.**
Dans cette capture, j'affecte la variable import_file du nom du fichier qui contient les adresses ip autorisée
Et un autre variable qui contient la liste des adresses ip qui n'ont plus accès au contenu restreint
<img src="https://asanogo919-lab.github.io/Abdoulaye-Sanogo/img/python1.jpg" width="600" >
**Lire le contenu du fichier**
Ici j'affiche le contenu du fichier des adresses ip autorisée
With gère les erreurs et les ressources externes, donc je m'occupe plus de la fermeture du fichier
La fonction open pour ouvrir le fichier, en paramètre le chemin du fichier et l'action qu'on veut faire sur le fichier, juste le lire donc la lettre “r”
as file permet de stocker temporairement le contenu du fichier dans la variable file
Et ip_addresses=file.read() pour convertir le contenu en chaine de caractères
Et la dernière ligne pour afficher tout ca
<img src="https://asanogo919-lab.github.io/Abdoulaye-Sanogo/img/python2.jpg" width="600" >
**Convertir la chaîne en liste**
Je vais convertir le contenu de la variable ip_adresses qui est une chaîne de caractère en une liste pour permettre de le manipuler
<img src="https://asanogo919-lab.github.io/Abdoulaye-Sanogo/img/python3.jpg" width="600" >

**Supprimer les adresses IP qui figurent sur la liste de suppression**
Tres bien
Ici j'utilise une boucle for pour parcourir la liste des adresses ip autorise et une condition if qui vérifie a chaque fois que si une adresse ip autorisée se trouve dans la liste des adresses ip à retirer il le supprime de la liste des adresses ip autorise grâce à la méthode .remove(), cest cette ligne qui permet cela: ip_adresses.remove(element)
<img src="https://asanogo919-lab.github.io/Abdoulaye-Sanogo/img/python4.jpg" width="600" >
**Mettez à jour le fichier avec la liste révisée des adresses IP.**
Enfin je vais mettre à jour le fichier allow_list.txt
Je commence par convertir la liste des adresses ip autorise en une chaine de caractères avec cette instruction: ip_adresses=’ ’.join(ip_adresses)
J'ouvre le fichier allow_list.txt dont javais stocker le nom dans la variable import_file rappelez vous avec: with open(import_file, “w”) as file
Mais cette fois l'action qu'on veut faire c'est écrire dans le fichier donc on met “w”, notez que “w” écrase le contenu du fichier si on voulait ajouter un texte a la fin on aurait utiliser “a”
L'instruction: file.write(ip_adresses) permet d'écrire le contenu de ip_adresses dans file qui a ete utilise pour ouvrir notre fichier des adresses ip autorise
Et je termine par reouvrir le fichier pour le lire enfin de vérifier si tout s'est bien passé
<img src="https://asanogo919-lab.github.io/Abdoulaye-Sanogo/img/python5.jpg" width="600" >
**Résumé**
Voilà c'est terminé j'espère que vous avez compris les explications données tout au long
Ce projet montre mes compétences en python, je maîtrise les variables les fonctions conditionnelles les boucles et l'ouverture de fichier
Ce projet prouve ma capacité à appliquer python pour des tâches de cybersécurité
