# Git Cheat Sheet

Para que no me olviden las cosas en git+github


## Git básico

`git --help` 
`git status`
`git diff`

### Definiciones
`origin` == el repo de donde clonaste el repo -> tu cpu  
`remote` == el repo en git que no está en tu cpu -> en github


## Clonar un repo al cpu local

1) En la terminal ir al directorio done quieras que esté el código
2) `git clone <repo_url>` (ej: `git clone https://github.com/$ORG/$REPO.git` o mejor con un fork `git clone https://github.com/$TU_USER/$REPO.git`)


## Configurar un remote al fork

1) En la terminal, ve al cloned fork repo
2) Dale a `git remote -v` para listar los remote repos configurados a tu fork
3) Especifica un nuevo remote upstream repo que tu fork mira `git remote add upstream https://github.com/$ORG/$REPO.git`
4) Verifica que se seteó correctamente corriendo `git remote -v` otra vez (deben haber dos remotes con origin para el fork y dos remotes para el upstream en el repo original de la organización)


## Commiting al fork

1) `git add <file>`
2) `git commit -m 'mensage'`
3) `git push`


## Update los archivos locales (del fork)

`git pull` O `git fetch && git checkout master`


## Update el fork al repo original (upstream)

1) `git fetch upstream`
2) `git checkout master`
3) `git rebase upstream/master`
4) `git push -f origin master`


## Branches (features)

### Crear un nuevo branch

1) Checkout un nuevo branch (ej: branch-nuevo) `git checkout -b branch-nuevo`
2) Push el branch para que mire al remote `git push --set-upstream origin branch-nuevo`
3) Para moverte al branch-nuevo o master: `git fetch && git checkout branch-nuevo` o `git fetch && git checkout master`

### Borrar un branch despues del merge

1) Checkout todos los cambios primero y muevete al master: `git fetch && git checkout master`
2) Borra branch-nuevo: localmente `git branch -D branch-nuevo` y en github `git push --delete origin branch-nuevo`

### Going back a un commit en especifico y fast forwarding al upstream master
1) `git fetch upstream`
2) `git log`
3) `git reset --hard <commit SHA>`
4) `git pull -ff upstream master`


## Reverting a un commit en específico (aveces uno la caga)
1) `git reflog`
2) `git push origin +<commit SHA>:master`
