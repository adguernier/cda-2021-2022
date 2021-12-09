# cda-2021-2022

## Initialiser un Dépot GIT
Se rendre dans le dossier du projet avec un terminal

``` bash
git init
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