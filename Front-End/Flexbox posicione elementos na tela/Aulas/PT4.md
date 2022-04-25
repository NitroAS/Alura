Responsivo


Site de Flexbox - https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_Flexible_Box_Layout/Aligning_Items_in_a_Flex_Container


Nele temos diversos ícones e nosso objetivo é decidir qual é a prioridade entre eles. O ícone mais importante, portanto, é o "Nosso APP" . Assim, é interessante colocá-lo mais acima em nossa lista!

Para alterar a distribuição dos elementos teríamos que abrir o html, encontrar o link e mudar o seu local. Dica; para alterar itens de posição utilize o atalho do MAC o Command + Ctrl. O problema é que alterar o html não é uma tarefa tão bacana.

Vamos tentar alterar a ordem dos itens utilizando o css. No cabeçalho nav nós já inserimos um flex, o que torna o cabecalhoPrincipal um flex-container. Podemos com o flex mudar a ordem.

Assim, nós desejamos alterar o cabecalhoPrincipal-nav-link-app e inserimos o order: -1:


https://css-tricks.com/snippets/css/a-guide-to-flexbox/


flex-grow: 1; = pega o espaço da pag é aumenta, muito bom usar para distribuir espaço vazio da pág
flex-grow: crescer mais um elemento ou outros

Assim, o tamanho do vídeo será distribuído de maneira a dividir o espaço com a parte de Vantagens. Se ao em vez de 1 tivéssemos colocado 2 o espaço total desta parte seria dividido em 3 cabendo ao vídeo 2/3 e ao Vantagens 1/2. Da mesma maneira podemos distribuir mais espaço para o Vantagens do que para o vídeo. Assim, colocando para o Vantagens um espaço maior, flex-grow: 3; teríamos 3/4 do espaço para o vantagens.

Nesse vídeo trabalhamos com flex-grow e sobre como ele divide o espaço vazio entre os flex-itens


flex-shrink: pega o espaço da pag é diminui
flex-grow: diminuir um elemento ou outros

Tanto o vídeo quanto o texto ficam extremamente comprimidos! O vídeo, porém, diminui em menores proporções, ele fica grande em comparação com o restante

Para resolver essa situação podemos utilizar o flex que diminui os elementos, no caso, é o flex-shrink. Assim, na classe correspondente ao vídeo, o .videoSobre-video nós vamos adicionar flex-shrink: 2. Assim, estaremos dizendo que nosso objetivo é que o item diminua duas vezes mais que os outros elementos:



----------------------------------------------

Quando colocamos display: flex em um elemento, o navegador passa a considerar esse elemento como um flex container, ou seja, cria todo aquele comportamento que vimos anteriormente no curso, os filhos ficam um do lado do outro e podemos aplicar propriedades para espaçá-los.

Os filhos de um flex container por sua vez também ganham um nome, são chamados de flex items.

Quando utilizamos flexbox temos que ficar atentos em quem colocamos as propriedades de espaçamento e distribuição do flex. Por exemplo, existem algumas propriedades que devem ser aplicadas à flex container e outras que devem ser aplicadas nos flex items.

------------------------------------------------


Quais são as propriedades que funcionam SOMENTE nos flex container e quais são as que funcionam nos flex items?

Existem diversos sites para consultar isso, como esse.


R:flex container:

justify-content, align-items, flex-direction, flex-wrap

flex items:

order, flex-grow, flex-shrink

A propriedade display: flex pode ser usada nos dois. Se for usada em um flex item esse elemento será tanto um flex item quanto um flex container.


R:flex container:

justify-content, align-items, display: flex,

flex items:

order, flex-grow, flex-shrink


O melhor a se fazer aqui é ter em mente que o ideal é sempre que necessário consultar a documentação através desse site.

Lá podemos ver claramente quais propriedades são aplicadas ao container e aos flex items, não há necessidade de ficar decorando, isso virá naturalmente com a prática.

Seguindo a documentação temos:

container:

display: flex
flex-direction
justify-content
flex-wrap
flex-flow
align-items
align-content
flex item:

order
flex-grow
flex-shrink
flex-basis
flex
align-self
Parabéns, você acertou!

