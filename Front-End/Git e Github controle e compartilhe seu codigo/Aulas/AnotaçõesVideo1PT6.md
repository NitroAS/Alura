Logados como Vinicius, já entendemos que, se utilizarmos git log -p, conseguiremos ver o que foi alterado em código commit a commit. Existe um comando do Git, bem interessante e poderoso, que é o git diff, capaz de exibir estas diferenças. Ao tentarmos executá-lo, porém, nada é exibido.

Isso porque por enquanto não há nada alterado no nosso código, que não tenha sido salvo. Então, para entendermos as diferenças entre dois commits, precisaremos informar quais são, no caso, ea539b3 até (..) 6ca12ac. Por meio deste comando, visualizamos todas as alterações feitas, marcadas em cores diferentes.

Além disso, caso estejamos modificando algo, como acresentando um novo curso na listagem, no código, e queiramos verificar o que foi alterado, poderemos simplesmente usar o git diff, que nos mostra o que foi alterado e que ainda não foi adicionado para commit. Mas a partir do momento em que adicionamos o arquivo, este comando não nos mostra mais o que existe de diferente.

Traremos o arquivo de volta após git status com git reset HEAD index.html, e com git status conferiremos que ele está pronto para ser adicionado ao commit. Vamos desfazer as alterações com git checkout -- index.html. Desta forma, conseguimos começar a analisar com maior controle todas as alterações que foram adicionadas durante o desenvolvimento de um projeto



git diff - para ver a diferença de  versões de Hash