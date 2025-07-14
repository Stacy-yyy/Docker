## Information système et aide

**Affiche les versions client et serveur de Docker :**
```bash
docker version
```

**Donne toutes les infos sur ton système Docker :**
```bash
docker info
```

**Liste l'aide générale des commandes Docker :**
```bash
docker help
```

**Affiche l’aide spécifique d’une commande :**
```bash
docker commande --help
```

## Images (Docker Image)

**Télécharge une image depuis Docker Hub :**
```bash
docker pull image
```

**Construit une image Docker à partir d’un Dockerfile :**
```bash
docker build -t mon_image .
```

**Liste toutes les images disponibles localement :**
```bash
docker images
```

**Supprime une image :**
```bash
docker rmi nom_image
```

**Renomme une image :**
```bash
docker tag nom_image nouveau_nom:tag
```

**Sauvegarde une image dans un fichier .tar :**
```bash
docker save image > fichier.tar
```

**Restaure une image depuis un fichier .tar :**
```bash
docker load < fichier.tar
```

**Donne les détails techniques d’une image :**
```bash 
docker inspect image
```

## Conteneurs (Docker Container)

**Lance un conteneur à partir d'une image :**
```bash
docker run image
```

**Lance un conteneur interactif avec terminal :**
```bash
docker run -it image bash
```

**Lance un conteneur en arrière-plan :**
```bash
docker run -d image
```

**Redirige le port 80 du conteneur vers 8080 local :**
```bash
docker run -p 8080:80 image 
```

**Liste les conteneurs en cours d'exécution :**
```bash
docker ps
```

**Liste tous les conteneurs (même arrêtés) :**
```bash
docker ps -a
```

**Arrête un conteneur :**
```bash
docker stop container_id	
```

**Démarre un conteneur arrêté :**
```bash 
docker start container_id
```

**Redémarre un conteneur :**
```bash
docker restart container_id
```

**Supprime un conteneur :**
```bash
docker rm container_id 
```

**Affiche les logs d’un conteneur :**
```bash
docker logs container_id
```

**Ouvre un terminal dans un conteneur :**
```bash
docker exec -it container_id bash
```

**Se connecte à la sortie d’un conteneur :**
```bash
docker attach container_id
```

**Détaille le contenu du conteneur :**
```bash
docker inspect container_id
```

**Copie un fichier du conteneur vers l’hôte :**
```bash
docker cp conteneur:/src ./dest	
```

## Volumes (Docker Volume)

**Crée un volume de stockage :**
```bash
docker volume create nom_volume
```

**Liste les volumes disponibles :**
```bash
docker volume ls
```

**Supprime un volume :**
```bash
docker volume rm nom_volume
```

**Détaille les informations d’un volume :**
```bash
docker volume inspect nom_volume
```

## Réseaux (Docker Network)

**Liste les réseaux Docker existants :**
```bash
docker network ls
```

**Crée un réseau Docker personnalisé :**
```bash
docker network create nom
```

**Supprime un réseau :**
```bash
docker network rm nom
```

**Détails techniques d’un réseau :**
```bash
docker network inspect nom
```

**Connecte un conteneur à un réseau :**
```bash
docker network connect res conteneur
```

**Déconnecte un conteneur d’un réseau :**
```bash
docker network disconnect res conteneur
```

## Nettoyage Docker

**Supprime tous les éléments inutilisés :**
```bash
docker system prune
```

**Supprime tout y compris les images non utilisées :**
```bash
docker system prune -a
```

**Supprime les images inutilisées :**
```bash
docker image prune
```

**Supprime les conteneurs arrêtés :**
```bash
docker container prune
```

**Supprime les volumes non utilisés :**
```bash
docker volume prune
```

**Supprime les caches de construction :**
```bash
docker builder prune
```

## Docker Compose

**Lance les services définis dans docker-compose.yml :**
```bash
docker-compose up
```

**Lance les services en arrière-plan :**
```bash
docker-compose up -d
```

**Arrête et supprime les conteneurs, réseaux, volumes :**
```bash
docker-compose down
```

**Reconstruit les images définies dans le fichier :**
```bash
docker-compose build
```

**Affiche les services en cours d’exécution :**
```bash
docker-compose ps
```

**Affiche les logs de tous les services :**
```bash
docker-compose logs
```

**Exécute une commande dans un service :**
```bash
docker-compose exec svc bash
```

**Arrête ou démarre les services :**
```bash
docker-compose stop/start
```

## Docker Swarm

**Initialise un nœud en tant que manager :**
```bash
docker swarm init
```

**Rejoint un cluster Swarm (comme worker ou manager) :**
```bash
docker swarm join --token TOKEN
```

**Quitte le cluster Swarm :**
```bash
docker swarm leave
```

**Quitte le cluster de force (pour un manager) :**
```bash
docker swarm leave --force
```

**Liste tous les nœuds du cluster :**
```bash
docker node ls
```

**Détails d’un nœud :**
```bash
docker node inspect ID
```

**Passe un nœud worker en manager :**
```bash
docker node promote ID
```

**Rétrograde un manager en worker :**
```bash 
docker node demote ID
```

**Crée un service (un conteneur managé par Swarm) :**
```bash
docker service create --name nom_image
```

**Liste tous les services actifs :**
```bash
docker service ls
```

**Liste les tâches (conteneurs) d’un service :**
```bash
docker service ps SERVICE
```

**Détails techniques sur un service :**
```bash 
docker service inspect SERVICE
```

**Supprime un service :**
```bash
docker service rm SERVICE
```

**Déploie un stack complet (multi-services) :**
```bash
docker stack deploy -c fichier.yml nom
```

**Liste les stacks déployés :**
```bash 
docker stack ls
```

**Affiche les tâches d’un stack :**
```bash
docker stack ps nom
```

**Supprime un stack :**
```bash
docker stack rm nom
```

**Crée des configurations / secrets dans le cluster :**
```bash
docker config create / secret create
```
