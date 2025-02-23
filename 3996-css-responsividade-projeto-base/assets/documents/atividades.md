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