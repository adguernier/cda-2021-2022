# cda-2021-2022

## Initialiser un Dépot GIT
Se rendre dans le dossier du projet avec un terminal

``` bash
git init
```

## Avant le premier commit, il faut dire à GIT qui on est
``` bash
# seulement pour le projet
git config user.name "nomdutilisateur"

git config user.email "email@utilisateur.com"

# pour toute la machine
git config --global user.name "nomdutilisateur"

git config --global user.email "email@utilisateur.com"
 
```

## Pour faire un commit
Il faut ajouter ses fichiers à la zone Stage en faisant 
``` bash
git add chemin/vers/le/fichier.extension 
```
Pour ajouter plusieurs fichier:
``` bash
git add chemin/vers/le/fichier.extension add chemin/vers/un/autre/fichier.extension 
```
Pour tout ajouter
``` bash
git add . 
```

Ensuite, pour commit (ajouter une nouvelle entrée dans l'historique)
``` bash
git commit -m "Un message indiquant clairement ce que vous avez fait"
```

## Pusher son projet (envoyer sur le serveur)
Lier le projet à un dépot sur le serveur si ce n'est pas déjà fait
``` bash
git remote add origin https://github.com/username/repository.git
```

Il faut ensuite spécifier la branche par défaut:
``` bash
git branch -M main #ou master
```

Il ne reste plus qu'à envoyer les commit sur le serveur
``` bash
git push -u origin main
# ou si déjà fait
git push
```

## Pour voir qui a fait quoi
``` bash
git blame chemin/vers/le/fichier.extension
```

## Pour voir l'historique
``` bash
git log
# pour plus d'infos
git log --graph --stat
```

## Pour annuler une modification
Avant de commit !
Remet le fichier comme il était juste avant, dans le commit précédent
``` bash
git checkout -- chemin/vers/le/fichier.extension
#ou pour tout annuler 
git checkout -- .
```

## Revenir en arrière
``` bash
# Quand les modifications ne sont pas sur le serveur !
git reset HEAD^ # supprime le dernier commit et garde les modifications
git reset --hard HEAD^ # supprime le dernier commit et les modification

git reset SHA1 # supprime tous le commit jusqu'au SHA1

# quand les modifications sont sur le serveur
git revert SHA1 # commit à revert
```

## Pour mettre de côté
``` bash
git stash save 'un message pour expliquer votre travail' # met de côté

git stash apply # remet les modification dans la zone de travail

git stash pop # remet les modification dans la zone de travail et supprime le stash
```