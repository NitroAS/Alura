Para espaçar corretamente os elementos de um grid temos que realmente fazer contas com a boa e velha margin e width.

Se temos 3 elementos por linha podemos fazer algo do tipo:


HTML:

<div class="grid">

  <!-- primeira linha -->
  <div class="course"></div>
  <div class="course"></div>
  <div class="course"></div>

  <!-- segunda linha -->
  <div class="course"></div>
  <div class="course"></div>
  <div class="course"></div>

  <!-- terceira linha -->
  <div class="course"></div>
  <div class="course"></div>
  <div class="course"></div>

  <!-- quarta linha -->
  <div class="course"></div>
  <div class="course"></div>

</div>COPIAR CÓDIGO
CSS:

.grid {
  display: flex;
  flex-wrap: wrap;
}

.course {
  width: 31.3%;
  margin: 1%;
}



Nesse caso teriamos 3 .course por linha, cada um com width: 31.3% e margin: 1%.

De width isso totaliza: 31.3 * 3 = 93.9%.

De margin isso totaliza: 6% (1% à esquerda e 1% à direita de cada elemento).

No total temos: 93.9% + 6% = 99.9% que dá pra arredondar para 100%.