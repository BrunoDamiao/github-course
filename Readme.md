# GitHub #
1. Curso de Github para iniciantes

## install ##
    - link p/ downloads: https://git-scm.com/docs/gittutorial

## setup ##
    - git config --global user.name "name"
    - git config --global user.email "name@email.com"
    - git config --global core.editor vim
    - git config --list

## iniciando projeto git ##
    - git init      (partir do local)
    - git clone git@github.com:BrunoDamiao/github-course.git    (partir do servidor)

## essencial Git: ##

    > Básico:
        - git status
        - git [add, add *, add .]
        - git commint -m "comment"
        - git commint -am "comment" (add e commit direto)

    > Diff tracked / logs, show dos commits:
        - git diff [<nameFile>, --name-only]        (exibe alteração do file tracked[add])
        - git logs [--decorate, --graph, git shortlog sn]   (list all commits)
        - git show <hash_tag>       (exibe detalhes do commint hash)

    > Reset status / desfazer ação:
        - git rm --cached <filename>    ( reset status: stracked < unstracked )
        - git checkout <filename>       ( desfaz uma ação feita no arquivo )
        - git reset HEAD <filename>     ( reset status em edição)
        - git reset [--soft, --mixed, --hard] <filename>    ( desfaz commint hash )

## remote ##
    - git remote add origin [endereço repositório] (cincroniza local X remoto)
    - git remote -v (nome cicronização - origin)

## push e pull ##
    - git push      (upload code para o servidor)
    - git pull      (baixar code para seu pc)




## avançado Git: ##
    > Ramificação (Branch)
        - git checkout -b <nameBranch>      (criando branch local)
        - git branch                        (list branch local)
        - git checkout <nameBranch>         (navegando entre branch local)
        - git checkout -D <nameBranch>      (remover branch local)

        - git push origin :<nameBranch>     (remover branch server)

    > Merge / rebase (Branch)
        - git merge <nameBranch>            (mesclando branch, cria novo commit)
        - git rebase <nameBranch>           (rebase branch, add no final da arvore)

    > Criando .gitignore
        - cria o arquivo do tipo: .gitignore
        - defina os arquivos que não aparecem:
            *.php           (por extensão)
            files/          (por direretorio)
            nameFile.txt    (por nome do arquivo)

    > Criando checkpointer
        - git stash             (cria stash)
        - git stash apply       (add stash ao branch)
        - git stash list        (list stash)
        - git stash clear       (limpa todos stash)

    > Alias
        - git config --global alias.s status    (cria alias p/ função status)

    > Tag
        - git tag -a <nameTag> -m "mensagem tag"    (criando nova tag local)
        - git tag                                   (list tag local)
        - git tag -d 1.0.0                          (remove tag local)

        - git push origin master --tags             (create tag no server)
        - git push origin :<nameTag>                (remove tag no server)

    > Git Revert
        - git revert <hash_commit>     (inverter commit ruim para o bom, sem apagar o bom)



=======================================================================================



# Simulando processo de versionamento git a partir do repositorio
    |===========================================|=============================|
    |   > git clone [SSH repository]            |   clonando do repositorio   |
    |   > git [status - add - commint]          |   gerenciamento primario    |
    |   > git push -u origin master             |   enviando para servidor    |
    |                                           |                             |
    |   > git pull                              |   *Atualiza code local      |
    |===========================================|=============================|


# Simulando processo de versionamento git a partir do pc local
    |================================================|=============================|
    |   > git init                                   |   inicializa git            |
    |   > git [status - add - commint]               |   gerenciamento primario    |
    |   > git remote add origin [SSH repository]     |   criando remote origin     |
    |   > git push -u origin master                  |   enviando para servidor    |
    |================================================|=============================|

=======================================================================================

# Checklist 01: a partir do projeto local
    [] Criar dir do projetoX
    [] Inicialize o git
    [] Crie pager index.html do tipo ola mundo
    [] Crie remote origin
    [] Envie para servidor (push)

# Checklist 02: clonando projeto existente no servidor
    [] Clone projetoX na pasta projetoY
    [] Atualize pager index.html p/ tipo ola mundo! Obrigado Brasil
    [] Envie para servidor (push)
