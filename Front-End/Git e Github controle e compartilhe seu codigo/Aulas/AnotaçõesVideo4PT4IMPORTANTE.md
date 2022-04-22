Vimos um caso interessante acontecer: o Vinicius corrigiu um bug, isto é alterou um determinado trecho de código, porém a mesma tarefa foi executada também pela Ana. O que será que irá acontecer se juntarmos estes trabalhos? Dentre merge e rebase optaremos pelo primeiro, embora o resultado deles seja o mesmo.

Logados como Ana, utilizaremos git merge lista, e o Git nos informa que existe um conflito, e que houve falha no merge automático. É recomendado que corrijamos os conflitos primeiro, e depois commitemos o resultado. Ao voltarmos ao arquivo no VS Code, há indicações coloridas referenciando o conflito do Git, mas para o caso do uso de um editor de texto que não as tenha, focaremos somente no texto, ignorando as cores.

Entre as linhas <<<<<<< HEAD (Current Change) e =======, estão os dados do commit atual, na master. E entre as linhas ======= e >>>>>>> lista (Incoming Change), são os dados que estamos tentando trazer da branch lista. Ou seja, é exibida exatamente a diferença entre ambos. E tudo que precisamos fazer para corrigir este conflito é remover as informações indesejadas, sem que haja duplicação.

Editaremos e salvaremos o arquivo, retornaremos ao Git Bash e executaremos git status, e teremos a informação de que houve uma modificação em dois lugares, na branch atual e aquela que estamos tentando unificar. Feita a correção, simplesmente utilizaremos git add index.html, e então git commit para que o commit de merge seja realizado. Desta vez, se executarmos git log --graph, teremos a indicação do merge de lista. Em seguida, poderemos usar git push local master.

Vamos imaginar que o Vinicius corrija o título do curso de Vagrant para "Vagrant: Gerenciando máquinas virtuais", e nos logar como Vinicius, solicitar status, adicionar e commitar a alteração. Enviaremos as informações, e o que acontece é que enquanto o Vinicius estava trabalhando, a Ana enviou outra informação, o commit de merge.

É necessário, então, antes de enviarmos quaisquer dados e alterações, garantir que estamos trabalhando com a versão mais recente do código. Isso significa que, antes do envio, precisaremos trazer este código de volta (git pull local master). Agora, sim, será feito o merge da master que está no "servidor" com esta.

Assim, poderemos confirmar que tudo está como gostaríamos no VS Code, e depois enviar a alteração, com git push local master. Sempre que formos iniciar um desenvolvimento novo, sabemos que precisaremos verificar se há alguma alteração lá antes de enviarmos os dados. Antes da Ana continuar e fazer alguma alteração nova, ela sabe que é necessário verificar se não há nenhuma alteração ali, com git pull local master.

As informações são trazidas conforme esperado pelo Git Bash. Deste modo evitamos maiores conflitos, mas se acontecer, já vimos que conseguimos resolvê-los tranquilamente. Entendemos como trabalhar com repositórios remotos, em equipe, com branches independentes, e como uni-las, seja por meio do merge ou do rebase.

Existem estratégias bem específicas de quando e como criar uma branch, e podem surgir dúvidas quanto à criação de uma branch para cada funcionalidade ou feature nova. Sem entrar em detalhes — por não ser o foco deste curso — sabemos que branches são linhas de desenvolvimento, e aprendemos a lidar com elas.



Vimos como é simples resolver conflitos identificados pelo Git ao tentar realizar o merge.

Agora, gere um conflito e, ao invés de utilizar o merge, utilize o rebase para atualizar o master:

Vá para a branch titulo
Commite algo
Vá para a branch master, commite uma alteração na mesma linha
Execute git rebase titulo
Veja a saída do Git e utilize as informações que ela te der para, após corrigir o conflito, continuar o rebase.


Nesta aula, aprendemos:

Que uma branch (ou ramo) é uma linha de commits separada, e que pode ser utilizada para desenvolver funcionalidades independentes;
Que com branches separados, podemos evitar que o código de uma funcionalidade interfira em outra;
Como trazer o trabalho realizado em uma branch para outra branch, como por exemplo, o master, através do comando git merge;
Que o git merge gera um novo commit, informando que houve uma mescla entre duas branches;
Como trazer os commits de uma branch para outra, com o git rebase
Que o git rebase não gera um commit de merge, simplificando o nosso log;
Como os conflitos são apresentados pelo Git;
Como resolver os conflitos e manter apenas as alterações desejadas com o Git.