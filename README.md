# Working in pairs with Git 👯

> This repo is for students to practise committing, creating branches and merging them, and working in pairs with Git to get ready for the project

## 📝 Git cheat sheet

| Command                                   | Description                       | 
|-------------------------------------------|-----------------------------------|
| <code>git checkout -b branch-name</code>  | Create new branch AND move to it  | 
| <code>git checkout branch-name</code>     | Move to other branch              | 
| <code>git pull</code> | Brings all changes in branches from remote to local | 
| <code>git pull origin branch-name</code> | Bring changes from specific remote branch  | 
| <code>git stash</code> | Set aside changes without commiting them to change branches for a while  | 
| <code>git stash pop</code> | Bring back the changes you stashed  | 
| <code>git stash drop</code> | Dismiss the changes you stashed  | 
| <code>git add .</code> | Add the files you want to commit or use "." if it is all of them  | 
| <code>git commit -m "Commit name"</code> | Commit changes | 
| <code>git merge branch-name</code> | **From the receiving branch**, merge another branch  | 
| <code>git push origin branch-name</code> | Update branch also on remote repository  | 
| <code>git log --pretty=oneline</code> | See repository commits  | 


⭐️ To add a <code>tree</code> command to see the tree version of the git log, run in any terminal:
```bash
git config --global alias.tree "log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short"
```

After this, you can run, on any project with git:

```bash
git tree
```

To quit the command line and get out of the log, run:
```bash
:q
```

To practise and improve your Git skills, follow [this tutorial](https://githowto.com/history).

___
## 👯 Proceso para trabajar en pareja:

**A) Cuando voy a empezar una nueva tarea**
1. Cuando voy a iniciar una nueva tarea, me voy a la rama dev (<code>git checkout dev</code>) y hago un <code>git pull origin dev</code> para sincronizar mi rama local de dev con lo que haya podido subir mi compañer@ a github
2. Creo una rama con <code>git checkout -b branch-name</code> con el nombre del feature que voy a hacer, y lo marco en el kanban como "Doing". Una rama también puede ser un bug
```bash
git checkout dev
git pull origin dev
git checkout -b feature-name
```

**B) Cuando acabo la tarea**

Cuando acabo la tarea de esa rama, la guardo y después me llevo los cambios a dev:
```bash
git status
git add .
git commit -m "Closes#number descripción de qué hace la tarea"
git push origin branch-name  # si quiero subir la rama a github para tener la copia ahí, este paso es opcional
git checkout dev  # me voy a la rama compartida
git pull origin dev # vuelvo a comprobar si mi compañer@ ha hecho cambios mientras yo trabajaba
git merge branch-name # me traigo los cambios que he hecho yo a la rama dev y si hay conflictos los arreglo
git commit -m "merges branch-name into dev" # guardo los cambios
git push origin dev # subo los cambios a github para que se los pueda descargar mi compañer@
```
___
## 🎬 Practise time!
### Iteration one

- Miembro 1 del equipo debe forkear y clonar el repositorio. En Github, debe dar permisos al otro miembro para editar el repositorio (*Repo > Settings > Collaborators and teams*)
- El otro miembro (Miembro 2), se clona el repo **desde la cuenta de Github del compañero (no hacer dos forks)**.
- Miembro 1 crea una rama *dev*: <code>git checkout -b dev</code>
- Hacer una función en el archivo index.js, comitearlos en la rama dev y subir la rama *dev* a remoto (Github).

### Iteration two

- Miembro 2, para traerse lo que hay en remoto, hace <code>git pull</code>
- Miembro 2 se va a la rama *dev*: <code>git checkout dev</code>
- Desde aquí, crea una nueva rama: 





