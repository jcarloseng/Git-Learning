COMANDOS APRENDIDOS NO CURSO 'TRY GIT' (CODE SCHOOL)

Comandos Git (no Linux):

- git init

> Comando utilizado para criar um repositório (sera criada uma pasta ".git" na pasta do projeto)

- git status

> Verifica o status do repositório git, mostrando informações relevantes como: se há algum arquivo a ser comitado, etc.

- git add <file-name>

>  Comando utilizado para adicionar novos arquivos (ou novas versões de arquivos existentes) para serem comitados no git (staging area). Esses arquivos ainda não estão no repositório, eles estarão agurdando um comando de commit para serem enviados para lá.

- git commit -m "<type-any-message-here>"

> Esse comando 'comitará' os arquivos que estarão na staging area, ou seja, enviará os mesmos para o repositório git. nesse comando você deverá incluir uma breve mensagem mencionando as alterações que você realizou no aqruivo.

- git add '*txt'

> Esse comando será útil para adicionar vários arquivos com a mesma extensão (.txt) para a stanging area de uma só vez. eles estarão prontos para serem comitados futuramente.

- git log

> Esse comando mostra uma espécie de histórico de todos os comitts realizados. Eles estarão organizados por ordem de comitt (do mais atual até o mais antigo), cada um com sua respectiva mensagem (descrição da alteração).

- git remote add <remote-name> <repository-Url>

> Esse comando adiciona um repositorio remoto (nesse caso, o github) para que o repositório local seja enviado. o "remote-name" padrão utilizado é o "origin". 

- git push -u <remote-name> <branch-name>

> Esse comando diz ao git para onde os commits serão enviados quando o repositório estiver pronto para envio. Nesse caso será enviado para um repositório remoto (no Github). Como já informado anteriormente, por padrão o Remote Name é 'origin'. O nome padrão do branch local é 'master'. o comando '-u' será responsável pela memorização daquele comando específico, ou seja, se o comando enviado inicialmente for 'git push -u origin master', nas próximas vezes só será necessário digitar 'git push', pois o '-u' informado fará com que o git retome ao comando completo anteriormente digitado.

- git pull origin master

> Esse comando é responsável por 'puxar' alterações feitas no repositório remoto para o repositório local. Comando utilizado por exemplo quando novas pessoas são convidadas para participarem da elaboração de um projeto. Esses usuário usarão o comando 'git pull' para pegar esse arquivos, fazer suas alterações e depois usar o comando 'git push' para enviar as mudanças para o repositório remoto. Já é sabido que 'origin' é o remote name e 'master' é o branch name.

- git diff HEAD

> Comando resposável por mostrar as diferenças entre o repositório atual e a situação do mesmo no último commit. Por exemplo, caso seja realizado uma adição de novas alterações no repositório através do comando 'pull', a diferença entre essas novas alterações e o estado do ultimo commit será vista através do comando 'diff'. 'HEAD' é utilizado para fazer menção ao ponto do repositório no ultimo commit

- git diff --staged

> Outra maneira de ver as diferenças, desta vez mostrando as alterações que foram feitas dentro do arquivo. Esse referido arquivo deverá ter sido adicionado na staging area.

- git reset <file-name>

> Esse comando remove um arquivo da staging area. Desta forma esse referido arquivo não estará mais na lista de arquivos que estarão prontos para o commit.

- git checkout -- <target>

> Com esse comando o git desfaz todas as mudanças realizadas no repositório desde o último commit do arquivo mencionado em 'target'. Por exemplo, 'git checkout -- readme.txt' esse comando irá desfazer todas as mudanças realizadas no repositório desde o último commit do arquivo 'readme.txt'.

- git branch

> Comando usado para ver os branchs existentes. O branch que possui um asterisco do lado é o seu branch atual (em uso).

- git branch <branch-name>

> Esse comando cria um novo branch (ramo) com o nome a ser inserido no espaço "<branch-name>". Com isso é possível ter varios trabalhos no reposítorio de forma simultânea sem afetar o arquivo principal (do branch master).

- git checkout <branch-name>

> Comando responsável por mudar o branch atual (em uso) para o "branch-name". Por exemplo se o usuário estiver no branch master, com o comando "git checkout NewBranch" ele passará a estar no NewBranch.

- git checkout -b <new_branch>

> Esse comando desempenha a mesma função dos dois ultimos comandos citados acima, ou seja, ele cria o "new_branch" e já coloca esse branch criado como o branch atual [checkout].

- git rm '*.txt'

> Esse comando remove todos os arquivos com a extensão ".txt" do repositório. Ele também remove esses arquivos da staging area, caso eles estejam lá.

- git merge <branch-name>

> Esse comando mescla o conteúdo do "branch-name" para o branch atual. Dessa forma se o usuário está atualmente no branch master e deseja mesclar as mudanças feitas no "NewBranch" para o master, então ele deverá digitar "git merge NewBranch". Dessa forma as mudanças feitas em NewBranch serão passadas para o branch master.

- git branch -d <branch-name>

> Comando utilizado para deletar um branch. Por exemplo, caso o usuário queira deletar um branch chamado 'NewBranch', então o comando será "git branch -d NewBranch". Esse comando só funcionará se NewBranch já tiver sido mesclado.

- git branch -D <branch-name>

> Esse comando forçara que um branch que não tiver sido mesclado ainda seja excluido. O recurso '-D' é uma junção dos recursos '-d -f', sendo o último referente ao recurso '--force'.





