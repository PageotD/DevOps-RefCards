## Gestion des ressources

`kubectl create -f fichier.yaml`: Crée une ressource à partir d'un fichier de configuration YAML.</br>Exemple : kubectl create -f deployment.yaml crée un déploiement à partir du fichier "deployment.yaml".

`kubectl apply -f fichier.yaml`: Applique les changements à une ressource à partir d'un fichier de configuration YAML.</br>Exemple : kubectl apply -f deployment.yaml applique les modifications au déploiement à partir du fichier "deployment.yaml".

`kubectl get [ressource]`: Affiche les ressources.</br>Exemple : kubectl get pods affiche tous les pods.

`kubectl describe [ressource] [nom]`: Affiche les détails d'une ressource.</br>Exemple : kubectl describe pod my-pod affiche les détails du pod nommé "my-pod".

`kubectl delete [ressource] [nom]`: Supprime une ressource.</br>Exemple : kubectl delete pod my-pod supprime le pod nommé "my-pod".

## Interactions avec les pods

`kubectl logs [pod]`: Affiche les journaux d'un pod.</br>Exemple : kubectl logs my-pod affiche les journaux du pod "my-pod".

`kubectl exec -it [pod] -- [commande]`: Exécute une commande dans un pod.</br>Exemple : kubectl exec -it my-pod -- bash lance un shell interactif dans le pod "my-pod".

## Gestion des déploiements

`kubectl rollout [commande] [ressource]`: Gère les déploiements.
`kubectl rollout status deployment [nom]`: Affiche le statut du déploiement.</br>Exemple : kubectl rollout status deployment my-deployment.

`kubectl rollout history deployment [nom]`: Affiche l'historique des versions du déploiement.</br>Exemple : kubectl rollout history deployment my-deployment.

`kubectl rollout undo deployment [nom]`: Annule la dernière mise à jour du déploiement.</br>Exemple : kubectl rollout undo deployment my-deployment.

## Gestion des services

`kubectl expose [ressource] [nom] --port=port`: Expose une ressource en tant que service.</br>Exemple : kubectl expose deployment my-deployment --port=80.

`kubectl port-forward [pod] port_local:port_pod`: Redirige un port local vers un port d'un pod.</br>Exemple : kubectl port-forward my-pod 8080:80 redirige le port 8080 de la machine locale vers le port 80 du pod "my-pod".

## Gestion des configurations

`kubectl create configmap [nom] --from-file=fichier`: Crée une ConfigMap à partir d'un fichier.</br>Exemple : kubectl create configmap my-config --from-file=config.properties.

`kubectl create secret generic [nom] --from-literal=clé=valeur`: Crée un secret à partir d'une paire clé-valeur.</br>Exemple : kubectl create secret generic my-secret --from-literal=username=admin --from-literal=password=pass.

## Autres commandes utiles

`kubectl apply -f https://...`: Applique un fichier YAML distant.</br>Exemple : kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.2.0/aio/deploy/recommended.yaml installe le tableau de bord Kubernetes.

`kubectl get events`: Affiche les événements du cluster.

`kubectl version`: Affiche la version de kubectl et du serveur Kubernetes.