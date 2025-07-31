# Projeto de Exemplo Git
### Atividades - 31 de Julho de 2025

1. Link do repositório no GitHub: 
    https://github.com/andersonbfigueiredo/projeto-exercicio-git

2. O que o comando git init faz? 
    Local do Git Bash que foi criado o comando git init.

3. Qual a diferença entre git add e git commit? 
    add = Este comando serve para adicionar todos os arquivos criados dentro deste diretório.
    commit = Registro de alterações no git.

4. O que o comando git merge faz? 
    Serve para combinar diferente alterações de branchs em uma única branch.

5. Por que usamos git pull depois de uma alteração remota? 
    Para poder baixar alterações de repositório remoto na integra para o seu repositório local.

6. Você conseguiu resolver um conflito de merge? Como foi?

> ---------------------------------- COMENTÁRIOS DE RESPOSTA ----------------------------------
> --- AQUI FIZ O ENVIO DOS ARQUIVOS ONDE GEROU O CONFLITO
$ git push -u origin master
To https://github.com/andersonbfigueiredo/projeto-exercicio-git.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/andersonbfigueiredo/projeto-exercicio-git.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

> --- AQUI FIZ DOWNLOAD APÓS O CONFLITO
aluno@LAB-F08-03 MINGW64 ~/Documents/projeto-exercicio-git (master)
$ git pull
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 1010 bytes | 5.00 KiB/s, done.
From https://github.com/andersonbfigueiredo/projeto-exercicio-git
   72cf4ff..ad42787  master     -> origin/master
Auto-merging app.js
CONFLICT (content): Merge conflict in app.js
Automatic merge failed; fix conflicts and then commit the result.

> --- AQUI BUSQUEI O STATUS PARA VERIFICAÇÃO
aluno@LAB-F08-03 MINGW64 ~/Documents/projeto-exercicio-git (master|MERGING)
$ git status
On branch master
Your branch and 'origin/master' have diverged,
and have 1 and 1 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   app.js

no changes added to commit (use "git add" and/or "git commit -a")

> --- AQUI ADD O APP.JS APÓS O STATUS E ESCOLHA NO VSCODE DA ALTERAÇÃO DO MERGE
aluno@LAB-F08-03 MINGW64 ~/Documents/projeto-exercicio-git (master|MERGING)
$ git add app.js

> --- AQUI BUSQUEI O STATUS PARA VERIFICAÇÃO NOVAMENTE
aluno@LAB-F08-03 MINGW64 ~/Documents/projeto-exercicio-git (master|MERGING)
$ git status
On branch master
Your branch and 'origin/master' have diverged,
and have 1 and 1 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)

All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
        modified:   app.js

> --- AQUI GEREI O COMENDO MERGE APÓS O STATUS PARA VERIFICAÇÃO
aluno@LAB-F08-03 MINGW64 ~/Documents/projeto-exercicio-git (master|MERGING)
$ git merge
fatal: You have not concluded your merge (MERGE_HEAD exists).
Please, commit your changes before you merge.

> --- AQUI GEREI O COMMIT SELECIONANDO BRANCH DEVIDA
aluno@LAB-F08-03 MINGW64 ~/Documents/projeto-exercicio-git (master|MERGING)
$ git commit -m "Resolvendo o desafio fazendo o Merge do upload da branch local com a do navegador"                                   [master a898075] Resolvendo o desafio fazendo o Merge do upload da branch local com a do navegador

> --- AQUI BUSQUEI O STATUS PARA VERIFICAÇÃO
aluno@LAB-F08-03 MINGW64 ~/Documents/projeto-exercicio-git (master)
$ git status
On branch master
Your branch is ahead of 'origin/master' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

> --- AQUI FIZ UM PUSH PARA FINALIZAR
aluno@LAB-F08-03 MINGW64 ~/Documents/projeto-exercicio-git (master)
$ git push -u origin master
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 6 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 789 bytes | 789.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/andersonbfigueiredo/projeto-exercicio-git.git
   ad42787..a898075  master -> master
branch 'master' set up to track 'origin/master'.

> ---------------------------------- COMENTÁRIOS DE RESPOSTA ----------------------------------

7. Você teve alguma dificuldade durante o exercício? 
    Sim, lembrar de todos os comandos.
