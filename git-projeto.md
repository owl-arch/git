## Projeto já existente no repositório
```bash
# download do repositório do GitHub para sua maquina
# Replace `owner/repo` with the owner and name of the repository to clone
git clone https://github.com/owner/repo.git

# navegue para o diretório `repo`
cd repo

# crie uma nova branch para armazenar qualquer nova mudança 
git branch my-branch

# troque para a sua branch (desenvolvimento)
git checkout my-branch

# make changes, for example, edit `file1.md` and `file2.md` using the text editor

# stage the changed files
git add file1.md file2.md

# take a snapshot of the staging area (anything that's been added)
git commit -m "my snapshot"

# push changes to github
git push --set-upstream origin my-branch
```


##  Iniciar um novo repositório e publicá-lo no GitHub
```bash
# create a new directory, and initialize it with git-specific functions
git init my-repo

# change into the `my-repo` directory
cd my-repo

# create the first file in the project
touch README.md

# git isn't aware of the file, stage it
git add README.md

# take a snapshot of the staging area
git commit -m "add README to initial commit"

# provide the path for the repository you created on github
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY-NAME.git

# push changes to github
git push --set-upstream origin main
```

## Contribuir para uma ramificação existente no GitHub
```bash
# change into the `repo` directory
cd repo

# update all remote tracking branches, and the currently checked out branch
git pull

# change into the existing branch called `feature-a`
git checkout feature-a

# make changes, for example, edit `file1.md` using the text editor

# stage the changed file
git add file1.md

# take a snapshot of the staging area
git commit -m "edit file1"

# push changes to github
git push
```

<br>
Referências:
- https://docs.github.com/en/get-started/using-git/about-git
