# 🐳 Atelier Docker — Partie Pratique

## 🎯 Objectif
Appliquer Docker à travers deux exercices simples :
1. Exécuter le conteneur **Hello World**
2. Lancer un **site web avec Nginx**

---

## 🧩 1. Exécution du conteneur "Hello World"

### Lancer le conteneur
```bash
docker run hello-world
```

🧠 Cette commande :
-Télécharge automatiquement l’image hello-world depuis Docker Hub (si elle n’existe pas en local)
-Crée un conteneur à partir de cette image
-Exécute un petit programme qui affiche le message :
“Hello from Docker!”

🟢 Si vous voyez ce message, Docker fonctionne correctement sur votre machine.


## 2. Déployer un site web avec Nginx
🔹 Étape 1 : Télécharger l’image Nginx
docker pull nginx

-Cette commande télécharge l’image officielle du serveur web Nginx depuis Docker Hub.

🔹 Étape 2 : Exécuter le conteneur
docker run -d -p 8080:80 nginx
🔍 Explications :
-d → lance le conteneur en arrière-plan
-p 8080:80 → redirige le port 80 du conteneur vers le port 8080 de votre machine

🔹 Étape 3 : Tester dans le navigateur
Ouvrez votre navigateur et entrez :
http://localhost:8080
🌟 Vous verrez la page d’accueil par défaut de Nginx : cela signifie que le serveur fonctionne bien à l’intérieur du conteneur.

## 🧹 3. Nettoyage des conteneurs et images

-Afficher tous les conteneurs :
docker ps -a

-Arrêter un conteneur :
docker stop <id_du_conteneur>

-Supprimer un conteneur :
docker rm <id_du_conteneur>

-Supprimer une image :
docker rmi nginx

## ✅ Résultat final

À la fin de cet atelier, vous avez :
-Exécuté votre premier conteneur Docker
-Déployé un petit site web avec Nginx
-Appris à gérer et nettoyer vos conteneurs

📘 Document préparé par : Salma Akajou — Solicode Tange
