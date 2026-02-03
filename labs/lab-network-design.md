# 🌐[LAB] Conception du Réseau et Configuration de la Sécurité

### 📝 Présentation du projet
Ce laboratoire pratique simule la création d'une infrastructure réseau pour l'entreprise **TechSafe, Ltd.** L'objectif était de concevoir un réseau segmenté, de calculer les adressages IP nécessaires et de sécuriser les flux sortants via des règles de pare-feu et de l'analyse de paquets.

---

### 🚀 Étape 1 : Architecture et Segmentation
Le réseau a été segmenté en trois départements distincts connectés à un commutateur central et un routeur pour assurer l'étanchéité et la gestion du trafic.

**Composants du réseau :**
* **Sous-réseaux :** Administration, Ventes, Informatique.
* **Équipements :** 1 Routeur, 1 Commutateur.

<img src="https://asanogo919-lab.github.io/Abdoulaye-Sanogo/img/ibm1.png" alt="Diagramme de réseau TechSafe" style="width:600px; border: 1px solid #ddd;" />
*Diagramme de réseau logique pour TechSafe, Ltd.*

---

### 🔢 Étape 2 : Plan d'adressage IP
Pour optimiser l'utilisation des adresses, j'ai calculé les masques de sous-réseau et les plages d'adresses IP pour chaque département.

<img src="https://asanogo919-lab.github.io/Abdoulaye-Sanogo/img/ibm2.png" alt="Blocage HTTP Pare-feu" style="width:600px;" />

---

### 🔍 Étape 3 : Analyse de Trafic avec Wireshark
J'ai effectué une capture de paquets pour analyser les flux **HTTP** et **HTTPS**. 
* **Objectif :** Comprendre la structure des données et identifier la différence entre le trafic en clair (port 80) et le trafic chiffré (port 443).

<img src="https://asanogo919-lab.github.io/Abdoulaye-Sanogo/img/ibm3.png" alt="Analyse Wireshark" style="width:600px;" />
*Capture Wireshark montrant l'analyse du flux de données d'un site web.*

---

### 🛡️ Étape 4 : Durcissement du Pare-feu (Windows Defender)
La phase finale consistait à sécuriser le poste de travail en bloquant les protocoles non sécurisés ou non autorisés.

#### 1. Blocage du trafic FTP (Sortant)
Le protocole FTP transmettant les identifiants en clair, j'ai créé une règle de sortie pour bloquer tout accès au serveur de test `ftp.dlptest.com`.
* **Résultat :** Tentative de connexion bloquée avec succès.

<img src="https://asanogo919-lab.github.io/Abdoulaye-Sanogo/img/ibm4.png" alt="Blocage FTP Pare-feu" style="width:600px;" />

#### 2. Blocage du trafic HTTP (Port 80)
Afin de forcer l'utilisation du HTTPS, j'ai configuré une règle bloquant tout trafic sortant sur le port 80 pour le site `httpforever.com`.
* **Résultat :** L'accès au site est devenu impossible après application de la règle, garantissant que seules les connexions sécurisées sont autorisées.

<img src="https://asanogo919-lab.github.io/Abdoulaye-Sanogo/img/ibm5.png" alt="Blocage HTTP Pare-feu" style="width:600px;" />

<img src="https://asanogo919-lab.github.io/Abdoulaye-Sanogo/img/ibm6.png" alt="Blocage HTTP Pare-feu" style="width:600px;" />
*Confirmation visuelle du blocage de l'accès HTTP via Windows Defender.*

---

### 🎯 Compétences Validées
* **Design Réseau :** Capacité à structurer un réseau d'entreprise.
* **Ingénierie IP :** Maîtrise du calcul de sous-réseaux.
* **Cyberdéfense :** Configuration de règles de pare-feu et filtrage de protocoles (FTP, HTTP).
* **Analyse :** Utilisation de Wireshark pour l'audit de trafic.
