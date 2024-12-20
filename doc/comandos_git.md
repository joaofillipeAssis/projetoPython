

# COMANDOS GIT


## Configuração Inicial
````bash
# Configurar nome e email
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"

# Verificar configurações
git config --list
````

## Comandos Básicos
````bash
# Iniciar um repositório
git init

# Verificar status dos arquivos
git status

# Adicionar arquivos ao staging
git add arquivo.txt    # arquivo específico
git add .              # todos os arquivos

# Criar commit
git commit -m "mensagem do commit"

# Ver histórico de commits
git log
git log --oneline     # formato resumido
````

## Branches
````bash
# Listar branches
git branch

# Criar nova branch
git branch nome-da-branch

# Mudar de branch
git checkout nome-da-branch
git switch nome-da-branch    # comando mais novo

# Criar e mudar de branch
git checkout -b nome-da-branch

# Deletar branch
git branch -d nome-da-branch
````

## Trabalhando com Remoto
````bash
# Adicionar repositório remoto
git remote add origin url-do-repositorio

# Enviar alterações para remoto
git push origin branch-name

# Baixar alterações do remoto
git pull origin branch-name

# Clonar repositório
git clone url-do-repositorio
````

## Merge e Rebase
````bash
# Fazer merge de branches
git merge nome-da-branch

# Fazer rebase
git rebase nome-da-branch
````

## Desfazer Alterações
````bash
# Descartar alterações não commitadas
git restore arquivo.txt
git checkout -- arquivo.txt  # comando antigo

# Desfazer último commit mantendo alterações
git reset --soft HEAD~1

# Desfazer último commit removendo alterações
git reset --hard HEAD~1

# Reverter um commit específico
git revert hash-do-commit
````

## Stash (Arquivos Temporários)
````bash
# Guardar alterações temporariamente
git stash

# Listar stashes
git stash list

# Recuperar último stash
git stash pop

# Recuperar stash específico
git stash apply stash@{numero}
````

## Visualização e Diferenças
````bash
# Ver diferenças
git diff
git diff arquivo.txt

# Ver commits de um autor
git log --author="nome-do-autor"

# Ver alterações de um arquivo
git blame arquivo.txt
````

## Tags (Versões)
````bash
# Criar tag
git tag v1.0.0

# Criar tag anotada
git tag -a v1.0.0 -m "mensagem"

# Listar tags
git tag

# Enviar tags para remoto
git push origin --tags
````

## Dicas Úteis
- Use `git help comando` para ver a documentação de um comando específico
- Use `git status` frequentemente para verificar o estado do seu repositório
- Faça commits pequenos e com mensagens claras
- Sempre verifique em qual branch está antes de começar a trabalhar
- Mantenha seu repositório local atualizado com `git pull` antes de começar a trabalhar