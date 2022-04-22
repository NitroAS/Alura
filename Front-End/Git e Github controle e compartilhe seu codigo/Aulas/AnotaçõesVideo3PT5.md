Se quisermos manter os commits feitos a partir deste ponto, será necessário criar uma nova branch. Reabriremos a ferramenta Visualizing Git para executarmos três git commit seguidos. Para verificarmos como estava o projeto durante o segundo commit, usaremos git checkout 54727de. Isto fará com que HEAD se locomova até ali, no lado direito da tela, e o estado do código esteja sendo exibido no segundo commit.

Se realizarmos qualquer alteração, incluindo outro git commit, o HEAD se locomoverá para um lugar sem nome, uma branch inexistente. E se fizermos git checkout master nunca mais conseguiremos acessar o commit em que estávamos anteriormente, que fica desanexado das linhas de desenvolvimento.

Repetiremos o comando git checkout 54727de e, se quisermos fazer alterações que sejam salvas a partir daqui, será necessário criar uma branch antes, a ser modificado a partir deste commit. Usaremos git checkout -b novo-branch, de forma a não estarmos mais desassociados da linha de desenvolvimento, o que se confirma se realizarmos um novo commit.

Poderemos fazer o git checkout master, mas se em algum momento quisermos voltar a trabalhar em novo-branch, basta usarmos o git checkout. Assim, conseguimos navegar entre os estados da nossa aplicação, de fato, "viajar no tempo" no projeto. Temos bastante conhecimento e poderemos fazer praticamente tudo o que é necessário para um trabalho do dia a dia, com o sistema de gerenciamento de versões.



git checkout 54727de - criar uma linha mas n fica associado 

git checkout -b novo-branch - e fica associada e com isso consegue mexer 


git checkout master  - volta para linha normal 




Nesta aula, aprendemos:

Que o Git pode nos ajudar a desfazer alterações que não vamos utilizar;
Que, para desfazer uma alteração antes de adicioná-la para commit (com git add), podemos utilizar o comando git checkout -- <arquivos>;
Que, para desfazer uma alteração após adicioná-la para commit, antes precisamos executar o git reset HEAD <arquivos> e depois podemos desfazê-las com git checkout -- <arquivos>;
Que, para revertermos as alterações realizadas em um commit, o comando git revert pode ser a solução;
Que o comando git revert gera um novo commit informando que alterações foram desfeitas;
Que, para guardar um trabalho para retomá-lo posteriormente, podemos utilizar o git stash;
Que, para visualizar quais alterações estão na stash, podemos utilizar o comando git stash list;
Que, com o comando git stash apply <numero>, podemos aplicar uma alteração específica da stash;
Que o comando git stash drop <numero> remove determinado item da stash;
Que o comando git stash pop aplica e remove a última alteração que foi adicionada na stash;
Que o git checkout serve para deixar a cópia do código da nossa aplicação no estado que desejarmos:
git checkout <branch> deixa o código no estado de uma branch com o nome <branch>;
git checkout <hash> deixa o código no estado do commit com o hash <hash>.
