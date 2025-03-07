# HowToUseGit
Passo a passo para subir um projeto para o Github

# INICIO - Criação do Projeto no GitHub
1. Crie um repositório no GitHub
Acesse GitHub.
Clique no ícone de "+" no canto superior direito e selecione "New repository".
Dê um nome ao repositório e configure como público ou privado.
### Não marque a opção de adicionar README, .gitignore ou licença (para evitar conflitos com seu projeto local).
Clique em Create repository.
Na próxima tela, copie a URL do repositório remoto.

# PASSO 1:
Vá para o PowerShell ou git Bash na raiz do seu projeto

Exemplo:
C:\Users\Aula\source\repos2\ECommerceDDD> ls
Diretório: C:\Users\Aula\source\repos2\ECommerceDDD

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        07/03/2025     20:30                ECommerceDDD.API
d-----        07/03/2025     20:14                ECommerceDDD.Domain
d-----        07/03/2025     20:15                ECommerceDDD.Infra
-a----        07/03/2025     20:40             76 .gitignore
-a----        07/03/2025     20:23           3027 ECommerceDDD.sln


PS C:\Users\Aula\source\repos2\ECommerceDDD> git init
Initialized empty Git repository in C:/Users/Aula/source/repos2/ECommerceDDD/.git/

# PASSO 2 - Add Origin:
PS C:\Users\Aula\source\repos2\ECommerceDDD> git remote add origin https://github.com/navarrowebapi/DDDSemRepositoryPattern.git

# PASSO 3: 
PS C:\Users\Aula\source\repos2\ECommerceDDD> git add .

# Ao dar o comando git add . e acontecer este erro abaixo:
error: open(".vs/ECommerceDDD/FileContentIndex/02f4d2b1-ce3e-45de-8988-d5e5b519709b.vsidx"): Permission denied
error: unable to index file '.vs/ECommerceDDD/FileContentIndex/02f4d2b1-ce3e-45de-8988-d5e5b519709b.vsidx'
fatal: adding files failed
PS C:\Users\Aula\source\repos2\ECommerceDDD> ls

# Reolva adicionando um arquivo ".gitignore" com este conteúdo:
# Ignorar arquivos e pastas do Visual Studio
.vs/
*.suo
*.user
*.cache

# PASSO 4 - git add . novamente:
PS C:\Users\Aula\source\repos2\ECommerceDDD> git add .

# PASSO 5 - git commit:
PS C:\Users\Aula\source\repos2\ECommerceDDD> git commit -m "commit inicial"

# PASSO 6 - Push
PS C:\Users\Aula\source\repos2\ECommerceDDD> git push -u origin master



