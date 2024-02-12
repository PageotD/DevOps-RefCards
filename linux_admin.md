## Naviguer dans le système de fichiers

`cd [répertoire cible]`: Changer de répertoire.</br>Exemple : `cd /var/www` pour accéder au répertoire `/var/www`.

`ls [options] [chemin]`: Lister le contenu du répertoire.</br>Exemple : ls -l pour afficher le contenu avec détails.

`pwd`: Afficher le chemin du répertoire actuel.</br>
Exemple : pwd pour afficher /home/user.

## Gestion des fichiers et répertoires

`mkdir [nom du répertoire]`: Créer un nouveau répertoire.</br>Exemple : mkdir new_directory pour créer un répertoire nommé "new_directory".

`touch [nom du fichier]`: Créer un nouveau fichier vide.</br>Exemple : touch new_file.txt pour créer un fichier vide nommé "new_file.txt".

`cp [options] source destination`: Copier des fichiers et répertoires.</br>Exemple : cp file1.txt file2.txt pour copier "file1.txt" vers "file2.txt".

`mv [options] source destination`: Déplacer des fichiers et répertoires.</br>Exemple : mv file1.txt /path/to/directory pour déplacer "file1.txt" vers un autre répertoire.

`rm [options] [chemin]`: Supprimer des fichiers et répertoires.</br>Exemple : rm old_file.txt pour supprimer le fichier "old_file.txt".

## Gestion des permissions

`chmod [options] permissions fichier`: Modifier les permissions d'un fichier ou d'un répertoire.</br>Exemple : chmod 755 script.sh pour donner la permission de lecture, écriture et exécution au propriétaire, et la permission de lecture et d'exécution aux autres.

`chown [options] utilisateur:groupe fichier`: Modifier le propriétaire et/ou le groupe d'un fichier ou d'un répertoire.</br>Exemple : chown user1:group1 file.txt pour définir l'utilisateur "user1" et le groupe "group1" comme propriétaire de "file.txt".

`chgrp [options] groupe fichier`: Modifier le groupe propriétaire d'un fichier ou d'un répertoire.</br>Exemple : chgrp group2 file.txt pour définir le groupe "group2" comme propriétaire de "file.txt".

## Gestion des processus

`ps [options]`: Afficher les processus en cours d'exécution.</br>Exemple : ps aux pour afficher tous les processus en cours d'exécution avec des détails.

`kill [options] PID`: Envoyer un signal à un processus (par exemple, kill -9 PID pour tuer un processus de force).</br>Exemple : kill 1234 pour arrêter le processus avec l'ID 1234.

`top`: Afficher les processus en cours d'exécution en temps réel.</br>Exemple : top pour afficher les processus en cours d'exécution et leurs performances en temps réel.

## Gestion des utilisateurs et des groupes

`adduser [utilisateur]`/`useradd [utilisateur]`: Ajouter un nouvel utilisateur.</br>Exemple : adduser newuser pour ajouter un nouvel utilisateur nommé "newuser".

`deluser [utilisateur]`/`userdel [utilisateur]`: Supprimer un utilisateur.</br>Exemple : deluser olduser pour supprimer l'utilisateur "olduser".

`passwd [utilisateur]`: Modifier le mot de passe d'un utilisateur.</br>Exemple : passwd username pour changer le mot de passe de l'utilisateur "username".

`addgroup [groupe]`/`groupadd [groupe]`: Ajouter un nouveau groupe.</br>Exemple : addgroup newgroup pour ajouter un nouveau groupe nommé "newgroup".

`delgroup [groupe]`/`groupdel [groupe]`: Supprimer un groupe.</br>Exemple : delgroup oldgroup pour supprimer le groupe "oldgroup".

## Gestion du réseau

`ifconfig [interface] [options]`: Afficher et configurer les interfaces réseau.</br>Exemple : ifconfig eth0 pour afficher la configuration de l'interface réseau "eth0".

`ping [hôte]`: Tester la connectivité réseau.</br>Exemple : ping google.com pour tester la connectivité avec le site "google.com".

`netstat [options]`: Afficher les connexions réseau, les tables de routage, les statistiques d'interface, etc.</br>Exemple : netstat -tuln pour afficher les ports en écoute sur le système.

`ss [options]`: Outil similaire à netstat, mais avec plus de fonctionnalités.</br>Exemple : ss -tuln pour afficher les ports en écoute sur le système.
Gestion des paquets :

`apt [commande] [paquet]`(Debian/Ubuntu)/`yum`(CentOS/RHEL)/`zypper`(openSUSE): Gestion des paquets (installation, mise à jour, suppression, etc.).</br>Exemple : apt update && apt install package_name pour mettre à jour les références des paquets et installer un nouveau paquet.

`dpkg [option] [paquet]`(Debian/Ubuntu)/`rpm`(CentOS/RHEL): Gestion des paquets individuels.</br> Exemple : dpkg -i package.deb pour installer un paquet Debian.

## Journalisation

`tail [options] fichier`: Afficher les dernières lignes d'un fichier journal.</br>Exemple : tail -n 20 /var/log/syslog pour afficher les 20 dernières lignes du journal système.

`grep [options] motif [fichier(s)]`: Rechercher des motifs dans les fichiers journaux.</br>Exemple : grep "error" /var/log/syslog pour rechercher toutes les lignes contenant le mot "error" dans le journal système.

`journalctl [options]`: Afficher les messages du journal du système.</br>Exemple : journalctl -u nginx.service pour afficher les journaux du service nginx.

## Gestion du démarrage

`systemctl [commande] [service]`: Gérer les services système (démarrage, arrêt, activation, désactivation, etc.).</br>Exemple : systemctl start service_name pour démarrer un service.

`service [service] [commande]`: Commande plus ancienne pour gérer les services système.</br>Exemple : service nginx restart pour redémarrer le service nginx.

## Sécurité

`ufw [options] [règle]`/`iptables`: Configuration du pare-feu.</br>Exemple : ufw allow 22 pour autoriser les connexions SSH entrantes.

`ssh`: Accès sécurisé à distance.</br>Exemple : ssh user@hostname pour se connecter à un serveur distant en tant qu'utilisateur