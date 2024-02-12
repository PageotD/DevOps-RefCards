## Scripts Shell

`#!/bin/bash`: Indique le chemin vers l'interpréteur de commandes à utiliser (déclaration du Shell).

`chmod +x script.sh`: Rend le script exécutable.

## Variables

`variable="valeur"`: Déclare une variable.</br>Exemple : nom="Jean" définit une variable nom avec la valeur "Jean".

`echo $variable`: Affiche la valeur d'une variable.</br>Exemple : echo $nom affiche "Jean".

`readonly variable`: Déclare une variable en lecture seule.</br>Exemple : readonly nom définit la variable nom comme en lecture seule.

## Entrée/Sortie

`read variable`: Lit l'entrée de l'utilisateur et la stocke dans une variable.</br>Exemple : read age lit l'entrée utilisateur et stocke la valeur dans la variable "age".

`echo "Texte" > fichier.txt`: Redirige la sortie vers un fichier (écrase le contenu).</br>Exemple : echo "Bonjour" > message.txt écrit "Bonjour" dans le fichier message.txt.

`echo "Texte" >> fichier.txt`: Redirige la sortie vers un fichier (ajoute au contenu existant).</br>Exemple : echo "Au revoir" >> message.txt ajoute "Au revoir" à la fin de fichier message.txt.

## Structures de contrôle

`if ... elif ... else ... fi`: Structure conditionnelle.
```bash
if [ condition ]; then
    instructions
elif [ autre_condition ]; then
    autres_instructions
else
    autres_instructions
fi
```

`for variable in liste; do ... done`: Boucle for.
```bash
for i in {1..5}; do
    echo $i
done
```

`while condition; do ... done`: Boucle while.
```bash
while [ $i -le 5 ]; do
    echo $i
    ((i++))
done
```

`case $variable in ... esac`: Structure de cas.
```bash
case $fruit in
    pomme)
        echo "C'est une pomme."
        ;;
    orange)
        echo "C'est une orange."
        ;;
    *)
        echo "Fruit non reconnu."
        ;;
esac
```

## Fonctions

```bash
maFonction() {
    instructions
}
```

Définit une fonction.
Exemple :
```bash
maFonction() {
    echo "Bonjour, $1 !"
}
```
`maFonction`: Appelle une fonction.</br>Exemple : maFonction "Jean" affichera "Bonjour, Jean !".

## Arguments et options

`$0, $1, $2, ...`: Récupère les arguments du script.

`$#`: Nombre total d'arguments passés au script.

`$@` et `$*`: Liste de tous les arguments passés au script.

`$?`: Code de sortie de la dernière commande exécutée.

Exemple : Si vous exécutez ./script.sh argument1 argument2, alors $1 sera "argument1" et $2 sera "argument2".

## Opérations

`expr`: Évalue une expression arithmétique.

`(( ... ))`: Effectue une évaluation arithmétique.

`let`: Effectue des opérations arithmétiques.</br>Exemple : let "resultat = 5 + 3" définit la variable "resultat" avec la valeur 8.

## Tests

`test` ou `[ ... ]`: Effectue des tests conditionnels.

`[[ ... ]]`: Version améliorée de test.</br>Exemple : if [[ $age -gt 18 ]]; then echo "Majeur"; fi teste si l'âge est supérieur à 18.

## Chaînes de caractères

`"${variable:position:longueur}"`: Extraction de sous-chaîne.</br>Exemple : echo ${nom:0:3} affiche les trois premiers caractères de la variable "nom".

`"${#variable}"`: Longueur de la chaîne.</br>Exemple : echo ${#nom} affiche la longueur de la variable "nom".

`"${variable/texte/remplacement}"`: Remplacement de texte.</br>Exemple : echo ${nom/ean/ane} remplace "ean" par "ane" dans la variable "nom".

`"${variable//texte/remplacement}"`: Remplacement global de texte.</br>Exemple : echo ${nom//e/E} remplace toutes les occurrences de "e" par "E" dans la variable "nom".

## Lecture et écriture de fichiers

`cat`, `head`, `tail`: Lecture de fichiers.</br>Exemple : cat fichier.txt affiche le contenu du fichier "fichier.txt".

`echo`, `printf`: Écriture dans des fichiers.</br>Exemple : echo "Texte" > fichier.txt écrit "Texte" dans le fichier "fichier.txt".

`grep`, `sed`, `awk`: Traitement de fichiers texte.</br>Exemple : grep "motif" fichier.txt recherche le motif dans le fichier "fichier.txt".