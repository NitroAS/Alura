na parte 2 eu alinhei o footer


No caso, o quadrado possui aproximadamente 250 px. Assim, podemos setar essa altura no código:

.rodapePrincipal-navMap-list {
    display: flex;
    flex-direction: column;
    height: 250px;
}


Ao fazer isso extrapolamos as alturas, assim, é preciso avisar de alguma forma que após acabar uma coluna deve haver uma quebra e passar para a próxima. Para que isso aconteça escrevemos flex-wrap: wrap:

.rodapePrincipal-navMap-list {
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    height: 250px;
}

Ao fazer isso teremos o seguinte:


Não foi fácil?! É muito mais simples do que utilizar qualquer outra propriedade de posicionamento! O flex facilita muitíssimo a nossa vida!

Um atalho que junta as duas propriedades de distribuição e a de quebra é a flex-flow e para ele passamos a direção, column, e a quebra, wrap: flex-flow: column wrap.


flex-wrap: wrap; - quebra a coluna do pai, sempre q n der ele quebra e criar outra coluna


Podemos distribuir os elementos dentro do pai de diversas formas, podemos por exemplo:

Colocar todo espaço à esquerda, jogando o conteúdo para direita com justify-content: flex-end.

Colocar todo espaço à direita, jogando o conteúdo para esquerda com justify-content: flex-start (que é o padrão).

Colocar todo espaço à esquerda e à direita, jogando o conteúdo para o meio com justify-content: center.

Colocar todo espaço entre os elementos como vimos antes usando justify-content: space-between.

E uma possibilidade bem interessante também é colocar o espaço em volta dos elementos. Podemos usar o justify-content: space-around para isso.