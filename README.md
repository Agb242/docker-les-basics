# Exercice : Déploiement d'un Site Statique avec Docker 

## Objectif :

Créer un site statique simple qui affiche "Équipe ? réussie !".
Déployer ce site sur Docker.
Chacun devra le mettre en ligne sur une instance.
Étapes de l’Exercice :

### 1. Prérequis :

Compétences Requises : VOLONTÉ
Ressources : Chaque étudiant doit avoir acces a play-with-docker

### 2. Création du Site Statique :


- Crée un nouveau répertoire pour le projet :
```
mkdir site-static && cd site-static
```
- Clone le dépôt contenant le site statique :
```
git clone https://github.com/Agb242/docker-les-basics
```

- Fichier HTML :

Observez votre  fichier index.html avec le contenu suivant :
```
vi index.html
```

- Modifier votre  fichier index.html :
```
vi index.html
```
- Inscrivez le nom de votre équipe :
```
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Équipe ici</title>
</head>
<body>
  <h1>Équipe numero ? réussie !</h1>
</body>
</html>
```
### 3. Dockerfile :

Observer votre fichier Dockerfile pour le site :
```
Cat Dockerfile
```

### 4. Construire et Lancer le Conteneur Docker :

- Construire l’image Docker :
```
sudo docker build -t site-static .
```
- Lancer le conteneur :
```
sudo docker run -d -p 80:80 site-static
```
5. Vérification :

Accède au site en utilisant l’IP publique de l’instance juste en haut sur OPEN PORT et saisir 80 :
http://<instance-adresse-public>
Le message exemple "Équipe 10 réussie !" devrait apparaître dans le navigateur.

-------------------------------------------------------------------------------
Suite Facultative afin de tester d'autres commandes docker :

Voici les 10 commandes Docker essentielles, avec des explications et des exercices simples pour les mettre en pratique :

### docker pull (Télécharge une image depuis un registre Docker.)

```
docker pull [nom_image]
```
Exemple : docker pull nginx

Exercice : Télécharge l'image nginx depuis Docker Hub.

```
docker pull nginx
```
### docker run (Lance un conteneur à partir d'une image.)

```
docker run [options] [nom_image]
```
Exemple : docker run -d -p 80:80 nginx

Exercice : Lance un conteneur nginx en mode détaché (-d) et mappe le port 80 du conteneur au port 80 de votre machine.

```
docker run -d -p 80:80 nginx
```
### docker ps (Affiche les conteneurs en cours d'exécution.)

```
docker ps
```
Exercice : Après avoir lancé le conteneur nginx, vérifie s'il est en cours d'exécution.

```
docker ps
```
- docker ps -a (Affiche tous les conteneurs, y compris ceux qui sont arrêtés.)

```
docker ps -a
```
Exercice : Affiche tous les conteneurs, qu'ils soient en cours d'exécution ou arrêtés.

```
docker ps -a
```
### docker stop (Arrête un conteneur en cours d'exécution.)

```
docker stop [nom_conteneur ou ID]
```
Exercice : Arrête le conteneur nginx que tu viens de lancer.

```
docker stop [nom_conteneur ou ID]
```
### docker start (Démarre un conteneur arrêté.)

```
docker start [nom_conteneur ou ID]
```
Exercice : Redémarre le conteneur nginx que tu as arrêté.
```
docker start [nom_conteneur ou ID]
```
docker rm (Supprime un conteneur arrêté.)
```
docker rm [nom_conteneur ou ID]
```
Exercice : Supprime le conteneur nginx arrêté.

```
docker rm [nom_conteneur ou ID]
```
### docker rmi (Supprime une image Docker.)

```
docker rmi [nom_image ou ID]
```
Exercice : Supprime l'image nginx téléchargée.

```
docker rmi nginx
```

### docker exec (Exécute une commande dans un conteneur en cours d'exécution.)

```
docker exec -it [nom_conteneur ou ID] [commande]
```
Exemple : docker exec -it nginx bash

Exercice : Lance un shell interactif dans le conteneur nginx.

```
docker exec -it [nom_conteneur ou ID] bash
```

### docker logs (Affiche les logs d'un conteneur.)

Exercice : Affiche les logs du conteneur nginx.

]```
docker logs [nom_conteneur ou ID]
```
