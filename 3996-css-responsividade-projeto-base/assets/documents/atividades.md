Recentemente, você ficou responsável por otimizar o site da empresa para ser mais responsivo, especialmente em relação às imagens. O site precisa funcionar bem em uma variedade de dispositivos, desde smartphones até desktops. Você tem várias opções para implementar essa funcionalidade, incluindo o uso de media queries, breakpoints, srcset e medidas relativas. Sua tarefa é escolher a melhor abordagem e justificar sua decisão.

Qual das seguintes abordagens você escolheria para garantir que as imagens no site da Alura Start sejam responsivas e otimizadas para diferentes dispositivos, e por quê?

```xml
Utilizar a tag <picture> e a tag <img> com diferentes fontes de arquivo de imagem.
```
> Esta abordagem é robusta e permite um controle fino sobre quais imagens são carregadas em diferentes resoluções.

```xml
Utilizar o atributo srcset na tag <img> para fornecer diferentes resoluções da mesma imagem.
```
> O atributo srcset permite que o navegador escolha a melhor resolução de imagem com base na densidade de pixels do dispositivo.

---
<br>

---

Você é uma pessoa desenvolvedora júnior na Alura Start, uma empresa que ensina tecnologia nas escolas. Seu próximo projeto é criar uma página web responsiva para um evento escolar. A página deve exibir uma imagem de banner que se adapta a diferentes tamanhos de tela usando media queries e breakpoints. Você precisa garantir que a imagem seja exibida corretamente em dispositivos móveis, tablets e desktops.

Qual das opções abaixo melhor implementa uma imagem de banner responsiva que se adapta a diferentes tamanhos de tela?

```html
<img src="banner.jpg" srcset="banner-small.jpg 600w, banner-medium.jpg 1200w, banner-large.jpg 1800w" sizes="(max-width: 600px) 100vw, (max-width: 1200px) 50vw, 33vw">
```
> Esta opção usa o atributo srcset para fornecer diferentes versões da imagem para diferentes tamanhos de tela e o atributo sizes para definir como a imagem deve se comportar em diferentes breakpoints.

---
<br>

---

Você está trabalhando na Alura Start. Sua tarefa é criar um layout fluido para a seção "Quem Somos" do site da empresa. O layout deve ser responsivo, adaptando-se bem a diferentes tamanhos de tela. Você já tem um código base, mas precisa ajustá-lo para que a seção "Quem Somos" se comporte de maneira diferente em dispositivos móveis.

```css
.quem-somos {
  display: flex;
  justify-content: space-between;
  padding: 7rem 0;

  @media (max-width: 768px) {
    flex-direction: row-reverse;
    padding: var(--padding-xl) 0;
  }
}
```

Como você ajustaria o código CSS acima para que a seção "Quem Somos" tenha uma direção de coluna em telas menores que 768px e um espaçamento de 5rem no topo e na base?

```css
.quem-somos {
 @media (max-width: 768px) {
    flex-direction: column;
    padding: 5rem 0;
 }
}
```
> Esta alternativa ajusta a direção do flex para coluna e define o espaçamento de 5rem no topo e na base para telas menores que 768px.

---
<br>

---

Seu objetivo é criar um layout fluido que se adapta bem tanto em dispositivos móveis quanto em telas maiores. Para isso, você decide usar media queries e operadores para ajustar o comportamento do layout. O código base que você está utilizando é o seguinte:

```css
@media (max-width: 768px), (orientation: landscape) {
  flex-wrap: wrap;
  justify-content: space-around;
}
```
Considerando o código base fornecido, qual das seguintes opções melhor descreve o comportamento do layout quando a largura da tela é menor ou igual a 768px ou quando a orientação da tela é paisagem?

```xml
O layout irá aplicar flex-wrap: wrap e justify-content: space-around quando a largura da tela for menor ou igual a 768px ou quando a orientação da tela for paisagem.
```
> Perfeito, o operador , (vírgula) funciona como um "ou", aplicando os estilos se qualquer uma das condições for verdadeira.

---
<br>

---

Você foi encarregado de ajustar o tamanho das fontes para diferentes dispositivos mobile. O código base que você tem é o seguinte:

```css
h1,h2,h3,h4,h5 {
@media (max-width: 768px) {
  @media (max-width: 425px) {
    font-size: 2.5rem;
  }
  &:not(h1) {
    font-size: var(--fonte-size-l);
  }
}
}
```

Com base no código fornecido, qual será o tamanho da fonte de um título <h1> em um dispositivo com largura de 400px?

```css
2.5rem
```
> O código aninhado @media (max-width: 425px) define font-size: 2.5rem para dispositivos com largura até 425px, incluindo 400px.

---
<br>

---

Você é uma pessoa desenvolvedora na Alura Start e recebeu como tarefa adicionar uma animação suave que apareça ao interagir com o scroll da página, destacando os serviços oferecidos. Para isso, você decidiu usar @keyframes para definir a animação e aplicá-la usando animation e animation-timeline.

```css
@keyframes appear {
  // O que irá aqui ?
}
.element {
 // O que irá aqui ?
}
```
Como você criaria uma animação que faz os elementos da página inicial aparecerem suavemente quando a página é visualizada?

```css
@keyframes appear {
  from { opacity: 0; }
  to { opacity: 1; }
}
.element {
  animation: appear linear;
  animation-timeline: view();
  animation-range: entry 0;
}
```
> Esta alternativa usa @keyframes para definir a animação de opacidade e aplica corretamente as propriedades animation, animation-timeline e animation-range.