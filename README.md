# Cour Génie Logiciel : Test/Integration continue
## Utilisation de service de Versionning Git + Github

### Instalation

* Mac et Windows
Telecharger [ici](https://git-scm.com/downloads) et suivre l'instalation

* Linux ```sudo apt-get install git```

* Création du compte [Github](https://github.com/)

* *- faclultatif* pour ceux qui veulent ce connecter par la suite en SSH voici le [lien](https://help.github.com/articles/connecting-to-github-with-ssh/)

----


### Création d'un repo si aucun existant

* Initialisation d'un repository dans le dossier souhaité

```git init```

* si SSH ajout du lien vers le repo souhaité
```git remote add origin git@github.com:[User]/[Nom_repo].git```

* si https ajout du lien vers le repo souhaité
```git remote add origin https://github.com/[User]/[Nom_repo].git```

-----


### Iteration a chaque modification

* Ajout des fichiers souhaités dans le repository

```git add [le_nom_du_fichier]```

* une fois l'ensemble des fichiers souhaité ajouter création du commit

```git commit -m "[le message décrivant le commit]"```

* pousser vers le repository souhaité

```git push```

----



### Pull Request

- [x] Fork dans l'interface graphique de github

![Fork dans l'interface graphique de github](https://github.com/Tonow/GL-Test-CI/blob/master/Capture%20d'%C3%A9cran%20de%202018-01-07%2020-49-43.png)

- [x] Cloner le repository original

```git clone 	git@github.com:Tonow/GL-Test-CI.git```

- [x] Ajouter le chemin vers le Fork du repository qui est sur votre compte

```git remote add [votre-nom-github] 	git@github.com:[votre-nom-github]/GL-Test-CI.git".git```

> exemple après  ```git remote -vv```
* [votre-nom-github]	git@github.com:[votre-nom-github]/GL-Test-CI.git".git (fetch)
* [votre-nom-github] git@github.com:[votre-nom-github]/GL-Test-CI.git".git (push)
* origin	git@github.com:Tonow/GL-Test-CI.git".git (fetch)
* origin	git@github.com:Tonow/GL-Test-CI.git".git (push)

- [x] récupèrer toutes les données de ce projet que vous ne possédez pas déjà

```git fetch --all```

- [x]  récupère généralement les données depuis le serveur qui a été initialement cloné et essaie de les fusionner dans votre branche de travail actuel

```git pull```

- [x] Crée une branche de travail et basculer dessus

```git checkout -b [nom-de-la-branche-a-cree]```


- [x] une fois les modification faites et [commiter et pousser](https://github.com/Tonow/GL-Test-CI#iteration-a-chaque-modification) dans l'interface web de github crée une "New pull resquest"

![New pull resquest](https://github.com/Tonow/GL-Test-CI/blob/master/PR.png)

----


#### Fusionner les commit
[lien ohshitgit](http://ohshitgit.com/)

- si deja commit:
 * ```git log -5```
 * ```git rebase -i [hash d'un commit sain] ```
>  - squash [les commit a fusionner]
>  - choix du message du commit
 - ```git push -f```


- pas encore commit:

```git commit --amend```

----


### Documentation officiel:

[Branche](https://git-scm.com/book/fr/v1/Les-bases-de-Git-Travailler-avec-des-d%C3%A9p%C3%B4ts-distants)
