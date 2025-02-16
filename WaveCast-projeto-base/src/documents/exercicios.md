# Exercícios
Você foi encarregado de construir um site! Para construir o layout do projeto, foi escolhida a ferramenta CSS Grid para deixar o site responsivo e bem organizado.

Você precisa criar uma estrutura de website da seguinte forma:

1. Uma área de cabeçalho na parte superior;
2. Um menu lateral à direita na parte inferior;
3. Uma área de conteúdo principal à esquerda na parte inferior.

Essa é a estrutura HTML:

```html
<body>
    <header class="cabecalho">CONTEÚDO CABEÇALHO</header>
    <aside class="lateral">CONTEÚDO MENU LATERAL</aside>
    <main class="principal">CONTEÚDO PRINCIPAL</main>
</body>
```

```css
body {
    display: grid;
    grid-template-areas: 
    "header header"
    "main aside";
}

.cabecalho {     
    grid-area: header;
}

.lateral { 
    grid-area: aside;
}

.principal { 
    grid-area: main;
}
```

---

<br>

---

Você está remodelando o site de uma loja. O cliente pediu para você criar uma seção de um site onde todas as imagens devem ser alinhadas à parte inferior das células do grid, de maneira que, independentemente da altura da célula, as imagens sempre apareçam no final. Seu código-base inicial é o seguinte:

```css
.secao-imagens {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 20px;
}
```
Qual conjunto de propriedade + valor você deve adicionar à classe .secao-imagens para realizar a tarefa?

```css
align-items: end;
```
> A propriedade CSS align-items: end; alinha os itens ao final do contêiner na direção do bloco, que é o que nós queremos neste caso.

---

<br>

---

Você trabalha em uma equipe de desenvolvimento Front-end e repara que um colega de equipe escreveu o seguinte código para organizar quatro itens utilizando CSS Grid:

```css
.secao-horizontal .secao__cartoes {
  display: grid;
  grid-template-columns: 100px, 100px, 100px, 100px;
}
```

Sabendo que esse código é referente a uma grade de conteúdos que podem aumentar ou diminuir dinamicamente, assinale a alternativa que oferece a melhor opção de refatoração do código acima aplicando responsividade com CSS Grid.

```css
.secao-horizontal .secao__cartoes {
  display: grid;
  grid-template-columns: repeat(auto-fit, 100px);
}
```
> Unindo o repeat e auto-fit é possível criar um grid dinâmico que aumente ou diminua a quantidade de colunas de acordo com a largura do elemento pai.

---

<br>

---

Você está trabalhando na construção de um layout e se depara com o seguinte código:

```css
.secao-horizontal .cartao__imagem {
    grid-row: 1 / 4;
    grid-column: 1 / 2;
}

.secao-horizontal .cartao__botao {
    grid-row: 2 / 3;
    grid-column: 3 / 4;
}

.secao-horizontal .cartao__titulo {
    grid-row: 2 / 3;
    grid-column: 2 / 3;
}

.secao-horizontal .cartao__player {
    grid-row: 3 / 4;
    grid-column: 2 / 3;
}
```

Considere que a propriedade grid-row define a posição inicial e final de um elemento em linha, e a propriedade grid-column define a posição inicial e final de um elemento em coluna.

Assinale a alternativa que permite refatorar o código acima utilizando a propriedade grid-area.

```css
.secao-horizontal .cartao__imagem {
    grid-area: 1 / 1 / 4 / 2;
}

.secao-horizontal .cartao__botao {
    grid-area: 2 / 3 / 3 / 4;
}

.secao-horizontal .cartao__titulo {
    grid-area: 2 / 2 / 3 / 3;
}

.secao-horizontal .cartao__player {
    grid-area: 3 / 2 / 4 / 3;
}
```

> A substituição dos valores passados nas propriedades grid-row e grid-column para a propriedade grid-area está sendo aplicada corretamente, sendo os dois primeiros valores determinando a posição inicial de linhas e colunas e os dois últimos valores determinando a posição final de linhas e colunas respectivamente.

---

<br>

---

Em um processo seletivo, você foi indagado sobre duas páginas da internet:

<img src="https://cdn3.gnarususercontent.com.br/3368-grid/Aula5-img1.png.png">

Pensando estrategicamente, em qual você aplicaria Grid ou Flex e porquê?

```xml
Aplicaria display: flex na Imagem 1, pois os elementos estão organizados de forma unidirecional, ou seja, estão seguindo apenas um sentido. Na imagem 2, aplicaria display: grid já que há elementos alinhados tanto em linhas quanto em colunas, ou seja, de forma bidimensional.
```

> O display: grid é ideal para organizar elementos de forma bidimensional, e o display: flex é ideal para organizar elementos de forma unidimensional. Lembrando que essa é uma orientação de uso, com objetivo de ter um código mais simples e objetivo.