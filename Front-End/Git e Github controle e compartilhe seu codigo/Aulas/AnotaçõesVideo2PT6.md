que a partir do penúltimo commit — que acessaremos com git log -n 2 — seja cravada uma marcação, um checkpoint indicando que trata-se da versão 0.1, por exemplo. Em vários outros sistemas de controle de conteúdo, existe o conceito de tag, como quando você cria blogs e possui tags para marcar postagens que pertencem a categorias específicas.

No Git, é possível utilizar um conceito bastante similar, também denominado tag, capaz de marcar um ponto na aplicação que não pode ser modificado, fixo. Assim, após ser lançada, a versão 0.1 nunca deixará de ser a versão 0.1, e quaisquer alterações que forem feitas nela, serão incluídas na versão posterior.

Isso não quer dizer que faremos um código que não será mais editável, apenas que criaremos um marco para onde poderemos ir, e que terá um código correspondente àquele estado. E para criarmos uma tag, informaremos isto ao Git, com git tag -a, seguido do nome que damos a ela, v0.1.0, que poderia ser qualquer outro. Além disto, poderemos incluir uma mensagem. O comando completo ficaria, então: git tag -a v0.1.0 -m "Lançando a primeira versão (BETA) da aplicação de cursos".

Ao darmos "Enter", geramos uma tag, um marco na nossa aplicação. E se executarmos git tag, são exibidos todos estes marcos disponíveis, que no caso por enquanto se resume a apenas um. Já sabemos que é possível fazer push de master, ou de qualquer outra branch, como com git push local master e depois git push local v0.1.0 para enviarmos a tag ao servidor.

Para nos lembrarmos de um detalhe, vamos executar git remote -v. Estamos utilizando o GitHub, e temos um repositório local denominado origin, que faz menção a ele. Então, atualizaremos nosso código no GitHub com git push origin master. Também enviaremos a tag, com git push origin v0.1.0. Mas como será que visualizamos tags por meio do GitHub?

Atualizaremos a página do navegador, que nos informa que temos 17 commits, 1 branch (já que não enviamos as demais para lá), e 1 release, que é a versão pronta para ser lançada ou baixada por qualquer pessoa que queira utilizar em seu sistema. Poderemos ver a nossa mensagem, em qual commit a tag foi gerada, e baixar clicando no ícone com "zip".



git tag -a v0.1.0 -m "Lançando a primeira versão (BETA) da aplicação de cursos" - para lançcar uma versão n alterada/Fixa


serve para fazer uma release - baixar um aqui .ZIP


Nesta aula, aprendemos:

Que é possível visualizar quais alterações foram realizadas em cada arquivo, com o comando git diff;
Que, digitando apenas git diff, vemos as alterações em nossos arquivos que não foram adicionadas para commit (com git add);
Que é possível comparar as alterações entre duas branches com git diff <branch1>..<branch2>
Que é possível comparar as alterações feitas entre um commit e outro, através do comando git diff <commit1>..<commit2>;
Que o Git nos possibilita salvar marcos da nossa aplicação, como por exemplo, lançamento de versões, através do git tag;
Que o comando git tag -a é utilizado para gerar uma nova tag;
As Releases do GitHub, que são geradas para cada tag do Git criada em nosso repositório.