## Gestion des conteneurs

`docker run [options] [image] [commande] [arguments]`: Lance un nouveau conteneur.</br>Exemple : docker run -it ubuntu bash lance un conteneur Ubuntu avec un shell interactif.

`docker start [conteneur]`: Démarre un conteneur arrêté.</br>Exemple : docker start my_container démarre le conteneur nommé "my_container".

`docker stop [conteneur]`: Arrête un conteneur en cours d'exécution.</br>Exemple : docker stop my_container arrête le conteneur nommé "my_container".

`docker rm [conteneur]`: Supprime un conteneur arrêté.</br>Exemple : docker rm my_container supprime le conteneur nommé "my_container".

`docker ps [options]`: Affiche les conteneurs en cours d'exécution.</br>Exemple : docker ps affiche tous les conteneurs en cours d'exécution.

`docker images [options]`: Affiche les images Docker disponibles.</br>Exemple : docker images affiche toutes les images Docker téléchargées.

## Gestion des images

`docker build [options] [chemin]`: Construit une image Docker à partir d'un Dockerfile. Exemple : docker build -t my_image . construit une image à partir du Dockerfile dans le répertoire courant et lui donne le tag "my_image".

`docker pull [image]`: Télécharge une image Docker depuis un registre.</br>Exemple : docker pull ubuntu télécharge l'image Ubuntu depuis Docker Hub.

`docker push [image]`: Publie une image Docker dans un registre.</br>Exemple : docker push my_registry/my_image publie l'image "my_image" dans un registre nommé "my_registry".

`docker rmi [image]`: Supprime une image Docker.</br>Exemple : docker rmi my_image supprime l'image "my_image".

## Réseau et volumes

`docker network [options]`: Gère les réseaux Docker.</br>Exemple : docker network create my_network crée un nouveau réseau nommé "my_network".

`docker volume [options]`: Gère les volumes Docker.</br>Exemple : docker volume create my_volume crée un nouveau volume nommé "my_volume".

## Gestion des services (Docker Swarm)

`docker service [commande] [options]`: Gère les services dans un cluster Docker Swarm.</br>Exemple : docker service create --replicas 3 my_image crée un nouveau service avec 3 réplicas à partir de "my_image".

## Autres commandes utiles

`docker exec [options] [conteneur] [commande] [arguments]`: Exécute une commande dans un conteneur en cours d'exécution.</br>Exemple : docker exec -it my_container bash exécute un shell interactif dans le conteneur nommé "my_container".

`docker-compose [commande] [options]`: Gère les applications multi-conteneurs avec Docker Compose.</br>Exemple : docker-compose up -d démarre les services définis dans le fichier docker-compose.yml en arrière-plan.