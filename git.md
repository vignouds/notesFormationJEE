## Commandes Git
`git diff `

*Montre les différences entre des commits*

`git branch`

*Liste, créé, ou supprime des branches*

`git checkout -b mabranche`

*crée la branche mabranche et se met dessus*

`git stash`

*Met de côté les modifications actuelles*

`git stash pop`

*Récupère les modifications mises de côté et vide le stash*

`git revert`

*Réalise un commit qui fait l'inverse d'un autre commit (et donc l'annule)*

`git cherry-pick`

*Applique les changements d'un commit sur une autre branche*

`git remote`

*Manage set of tracked repositories*

`git fetch`

*Télécharge les modifications depuis le serveur sans les merge (pull = fetch + merge)*

`git tag`

*pour taguer un commit, on peut y aller via checkout*

`git push -u origin master`

*-u permet de lier le dépôt local et le dépôt distant*

## Commandes Unix
`echo "temp/" >> .gitignore`

*ajoute temp/ au fichier .gitignore ; git va donc ignorer tous les fichiers du dossier temp*

`mkdir`

*Crée un dossier*

## Conseils et mémo
Fichier .gitignore permet de lister les fichiers que Git doit ignorer.

Un commit doit être le plus atomique possible.

On ne travaille jamais sur le master.


## Liens
* [Documentation Git](https://git-scm.com/docs)
* [Cours d'Openclassrooms sur Git ](https://openclassrooms.com/courses/gerer-son-code-avec-git-et-github)
* [Cours d'Openclassrooms sur Markdown](https://openclassrooms.com/courses/redigez-en-markdown)
* [DTA](http://www.dta-ingenierie.fr/)
