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