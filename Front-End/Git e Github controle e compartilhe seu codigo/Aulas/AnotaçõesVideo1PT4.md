Estas ramificações do trabalho são uma das formas de com que podemos trabalhar, em relação aos branches do Git. Por padrão, se executarmos git branch no Git Bash, teremos um único branch, master, e é exatamente isto que o Git Bash nos mostra ao fim da linha. No entanto, poderemos criar outros. No caso de trabalharmos somente no título, por exemplo, utilizaremos o comando git branch titulo, que criará este branch, embora tenhamos que mudar para ela manualmente, com git checkout titulo.

A partir daí, estaremos trabalhando na linha de desenvolvimento titulo. Para isso ficar um pouco mais claro, utilizaremos uma ferramenta chamada Visualizing Git. Do lado esquerdo da página digitaremos os comandos, e o resultado destes serão exibidos do lado direito. Em se tratando do trabalho conjunto de Ana e Vinicius, teremos duas linhas de desenvolvimento distintas e independentes entre si.

Abriremos o VS Code e alteraremos o título, de <title>Cursos da Alura</title> para <title>Cursos de DevOps da Alura</title>. No Git Bash, estamos logados como Vinicius, e em titulo. Executaremos git status, verificaremos que há uma alteração, que adicionaremos com git add index.html, seguido de git commit -m "Alterando título da página".

Desta vez, se utilizarmos git log, dentre as informações que o comando nos traz, estão todos os commits realizados, incluindo o último, que é indicado como sendo o último commit realizado na master. O commit do título alterado só aparece na branch titulo, e se fizermos outra alteração no mesmo título, e refizermos todo o processo de adição, commit e verificação do log, teremos que até a mensagem "Renomeando curso de Integração Contínua" é feito na master.

Assim, somente a branch titulo possui as alterações feitas a partir de "Alterando título da página". Se precisarmos alterar algo no commit de "Renomeando curso de Integração Contínua", que não é influenciado pelo título, basta utilizarmos git checkout master para retornarmos à branch correspondente.

Feito isso, ao executarmos git log, não teremos acesso àqueles commits em titulo. Isso é bem interessante! Usaremos git checkout titulo para voltarmos, e passaremos a lidar com a Ana, que trabalhará com as listas de cursos. Criaremos, portanto, um branch com git branch lista, e depois faremos o checkout para a lista.

Entretanto, existe um atalho que cria um branch e já passar para ele: git checkout -b lista, que usaremos. Com isso, a Ana está na branch lista, então poderemos abrir o projeto da Ana no VS Code e adicionar um curso em uma nova lista, como <li>Kubernetes</li>, junto aos demais. No Git Bash, digitaremos git status, verificaremos que há uma modificação, adicionaremos todas elas com git add ., e commitaremos com git commit -m "Adicionando curso de kubernetes".

Assim, a Ana e o Vinicius estão trabalhando ao mesmo tempo em branches independentes de um mesmo projeto. Mas sabemos que em nosso repositório chamado local, por enquanto, temos apenas a branch master. Isso nos leva a assumir que esta branch é a nossa linha de desenvolvimento padrão, ou seja, nosso ramo principal, onde os códigos devem estar quando estiverem prontos, certo?

Então, como será que fazemos para trazer os dados das branches titulo e lista para a master?


https://git-school.github.io/visualizing-git/