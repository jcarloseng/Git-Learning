# COMANDOS APRENDIDOS NO CURSO [__TRY GIT__](https://try.github.io/)

### - Comandos Git (para Linux):

    $ git init

Comando utilizado para criar um repositório (sera criada uma pasta _/.git_ na pasta do projeto).

    $ git status

Verifica o status do repositório _git_, mostrando informações relevantes como: se há algum arquivo a ser comitado, etc.

    $ git add <file-name>

Comando utilizado para adicionar novos arquivos (ou novas versões de arquivos existentes) para serem comitados no _git_ (_staging area_). Esses arquivos ainda não estão no repositório, eles estarão agurdando um comando de _commit_ para serem enviados para lá.

    $ git commit -m "<type-any-message-here>"

Esse comando 'comitará' os arquivos que estarão na _staging area_, ou seja, enviará os mesmos para o repositório _git_. Nesse comando você deverá incluir uma breve mensagem mencionando as alterações que você realizou no aqruivo.

    $ git add '*txt'

Esse comando será útil para adicionar vários arquivos com a mesma extensão _.txt_ para a _stanging area_ de uma só vez. Eles estarão prontos para serem comitados futuramente.

    $ git log

Esse comando mostra uma espécie de histórico de todos os _commits_ realizados. Eles estarão organizados por ordem de _commit_ (do mais atual até o mais antigo), cada um com sua respectiva mensagem (descrição da alteração).

    $ git remote add <remote-name> <repository-Url>

Esse comando adiciona um repositório remoto (nesse caso, o [_github_](https://github.com/)) para que o repositório local seja enviado. O \<_remote-name_\> padrão é o _origin_. 

    $ git push -u <remote-name> <branch-name>

Esse comando diz ao _git_ para onde os _commits_ serão enviados quando o repositório estiver pronto para envio. Nesse caso será enviado para um repositório remoto. Como já informado anteriormente, por padrão o \<_remote-name_\> é _origin_. O nome padrão do _branch_ local é _master_. O comando __-u__ será responsável pela memorização daquele comando específico, ou seja, se o comando enviado inicialmente for **_git push -u origin master_**, nas próximas vezes só será necessário digitar **_git push_**, pois o **-u** informado fará com que o _git_ retome ao comando completo anteriormente digitado.

    $ git pull origin master

Esse comando é responsável por "puxar" alterações feitas no repositório remoto para o repositório local. Comando utilizado por exemplo quando novas pessoas são convidadas para participarem da elaboração de um projeto. Esses usuários usarão o comando **_git pull_** para pegar esse arquivos, fazerem suas alterações e depois usar o comando **_git push_** para enviar as mudanças para o repositório remoto. Já é sabido que **_origin_** é o _remote name_ e **_master_** é o _branch name_.

    $ git diff HEAD

Comando resposável por mostrar as diferenças entre o repositório atual e a situação do mesmo no último _commit_. Por exemplo, caso seja realizado uma adição de novas alterações no repositório através do comando _pull_, a diferença entre essas novas alterações e o estado do último _commit_ será vista através do comando _diff_. **_HEAD_** é utilizado para fazer menção ao ponto do repositório no último _commit_.

    $ git diff --staged

Outra maneira de ver as diferenças, desta vez mostrando as alterações que foram feitas dentro do arquivo. Esse referido arquivo deverá ter sido adicionado na _staging area_.

    $ git reset <file-name>

Esse comando remove um arquivo da _staging area_. Desta forma esse referido arquivo não estará mais na lista de arquivos que estarão prontos para o _commit_.

    $ git checkout -- <target>

Com esse comando o _git_ desfaz todas as mudanças realizadas no repositório desde o último _commit_ do arquivo mencionado em _\<target\>_. Por exemplo **_git checkout -- readme.txt_** , esse comando irá desfazer todas as mudanças realizadas no repositório desde o último _commit_ do arquivo _'readme.txt'_.

    $ git branch

Comando usado para ver os _branchs_ existentes. O _branch_ que possui um asterisco do lado é o seu _branch_ atual (em uso).

    $ git branch <branch-name>

Esse comando cria um novo _branch_ com o nome a ser inserido em _\<branch-name\>_. Com isso é possível ter vários trabalhos no reposítorio de forma simultânea sem afetar o arquivo principal (do _branch master_).

    $ git checkout <branch-name>

Comando responsável por mudar o _branch_ atual (em uso) para o informado  em _\<branch-name\>_. Por exemplo, se o usuário estiver no _branch master_, com o comando **_git checkout NewBranch_** ele passará a estar no _NewBranch_.

    $ git checkout -b <new_branch>

Esse comando desempenha a mesma função dos dois últimos comandos citados anteriomente, ou seja, ele cria o _\<new_branch\>_ e já coloca esse _branch_ criado como o _branch_ atual.

    $ git rm '*.txt'

Esse comando remove (apaga) todos os arquivos com a extensão _.txt_ do repositório. Ele também remove esses arquivos da _staging area_, caso eles estejam lá.

    $ git merge <branch-name>

Esse comando mescla o conteúdo do _\<branch-name\>_ para o _branch_ atual. Dessa forma se o usuário está atualmente no _branch master_ e deseja mesclar as mudanças feitas em _Newbranch_ para o _master_, então ele deverá digitar **_git merge Newbranch_**. Dessa forma as mudanças feitas em Newbranch serão passadas para o _branch master_.

    $ git branch -d <branch-name>

Comando utilizado para deletar um _branch_. Por exemplo, caso o usuário queira deletar um _branch_ chamado _Newbranch_, então o comando será **_git branch -d Newbranch_**. Esse comando só funcionará se _Newbranch_ já tiver sido mesclado (_merge_).

    $ git branch -D <branch-name>

Esse comando forçará que um _branch_ que não tiver sido mesclado ainda seja excluído. O recurso __-D__ é uma junção dos recursos __-d -f__, sendo o último referente ao recurso __--force__.
