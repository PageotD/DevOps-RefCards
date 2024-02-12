## Configurer Git

`git config --global user.name "Votre nom"`: Configure votre nom d'utilisateur.

`git config --global user.email "votre@email.com"`: Configure votre adresse e-mail.

`git config --global core.editor "nom_de_votre_editeur"`: Configure votre éditeur de texte par défaut.

`git config --list`: Affiche toutes les configurations Git.

## Créer et cloner un dépôt

`git init`: Initialise un nouveau dépôt Git dans le répertoire courant.

`git clone [url_du_depot]`: Clone un dépôt distant dans un nouveau répertoire.

## Gestion des modifications

`git status`: Affiche l'état des fichiers modifiés dans le répertoire de travail.

`git add [fichier]`: Ajoute un fichier modifié à l'index.

`git add .`: Ajoute tous les fichiers modifiés à l'index.

`git reset [fichier]`: Annule les modifications d'un fichier dans l'index.

`git diff`: Affiche les modifications entre l'index et le répertoire de travail.

## Validation des modifications

`git commit -m "message_de_commit"`: Valide les modifications de l'index avec un message.

`git commit -am "message_de_commit"`: Ajoute et valide tous les fichiers modifiés en une seule étape.

## Gestion des branches

`git branch`: Affiche la liste des branches locales.

`git branch [nom_de_branche]`: Crée une nouvelle branche.

`git checkout [nom_de_branche]`: Change de branche.

`git merge [nom_de_branche]`: Fusionne une branche dans la branche actuelle.

`git branch -d [nom_de_branche]`: Supprime une branche.

## Gestion des remotes

`git remote add [nom] [url]`: Ajoute un dépôt distant.

`git remote -v`: Affiche les dépôts distants configurés.

`git push [remote] [branche]`: Envoie les modifications locales vers un dépôt distant.

`git pull [remote] [branche]`: Récupère les modifications distantes et les fusionne avec la branche locale.

## Historique et annulation

`git log`: Affiche l'historique des commits.

`git log --oneline`: Affiche l'historique des commits sur une seule ligne.

`git reset HEAD~1`: Annule le dernier commit en conservant les modifications dans le répertoire de travail.

`git reset --hard HEAD~1`: Annule le dernier commit et supprime les modifications.

## Autres commandes utiles

`git stash`: Met de côté les modifications non validées.

`git stash pop`: Récupère les modifications mises de côté.

`git cherry-pick [commit]`: Applique un commit spécifique sur la branche actuelle.