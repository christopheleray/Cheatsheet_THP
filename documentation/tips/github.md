#Cheatsheet GitHub and branch: 

##Basic command:

`$ git init`

`$ git add .`

`$ git commit -m "your commit comment`

`$ git remote origin master YourRepoURl.git`

`$ git push -u origin master` 

-------

##Manage branch

`$ git branch : affiche toutes les branches de ton repo git, puis t'indique sur laquelle tu es actuellement`

`$ git branch nom_de_ta_feature : créé une branche au nom de nom_de_ta_feature`

`$ git checkout nom_de_ta_branche : se positionne sur la branche qui s'appelle nom_de_ta_branche `

`$ git branch : affiche toutes les branches de ton repo git, puis t'indique sur laquelle tu es actuellement`

`$ git merge nom_de_ta_branche : fusionne la branche nom_de_ta_branche avec la branche sur laquelle tu te trouves


##How to create a branch

`$ git branch nom_de_ta_feature`

`$ git checkout nom_de_ta_feature`

or create a branch and checkout the branch at the same time:

`$ ou bien git checkout -b ma_branch`

from there, work on your branch and don't forget to commit :) 
 
$ git branch -d ma-branche supprimer une branche

## How to merge a branch 

`$ git checkout master`

`$ git pull origin master`

`$ git checkout nom_de_ta_feature`

`$ git merge master`

`$ git checkout master`

`$ git merge nom_de_ta_feature`

`$ git push origin master`

If conflict, manage it

Tools to manage your conflict: 

`$ git mergetool vimdiff t`

[OpenClassRooms Tutorial](https://openclassrooms.com/courses/gerer-son-code-avec-git-et-github)

## Others commands: 

How to revert a commit

Je vous présente une de ces options : vous pouvez "revert" un commit, c'est-à-dire créer un nouveau commit qui fait l'inverse du précédent, avec la commande suivante :

`$ git revert SHADuCommit`

Modif a commit name: 

`$ git commit --amend -m "Votre nouveau message"`

Cancel all modifications done since the last commit: 

`$ git stash`

Delete a branch

`$ git branch -d nomdelabranche`

`$ git reset --hard‌`

Manage modification and see who did the modificaion: 

`$ git blame nomdufichier.extension`

##Others informations: 

Pour retrouver pourquoi cette modification a été faite, vous avez deux possibilités : 
1. Faire un git log et rechercher le commit dont le sha commence par 05b1233.  
2. Utiliser la commande git show qui vous renvoie directement les détails du commit recherché en saisissant le début de son sha : 

https://openclassrooms.com/fr/courses/2342361-gerez-votre-code-avec-git-et-github/2433726-evitez-des-commits-superflus
Comment faire pour ne pas perdre vos modifications en cours avant de passer à l'urgence à traiter ?
Et bien vous pouvez mettre de côté vos modifications en cours avec la commande :
git stash
Vous pouvez alors vous rendre dans la branche/le fichier que vous devez traiter à l'instant, finir et committer vos modifs. Une fois que vous avez réglé cette urgence, revenez sur la branche sur laquelle vous étiez en train de travailler, et récupérez les modifications que vous aviez mises de côté avec la commande : 
git stash pop

Si vous voulez garder les modifications dans votre stash, vous pouvez utiliser applyà la place de pop : 
git stash apply

##Other documentations

[Projet open source collaboration](https://openclassrooms.com/fr/courses/2342361-gerez-votre-code-avec-git-et-github/2433731-contribuez-a-des-projets-open-source)

