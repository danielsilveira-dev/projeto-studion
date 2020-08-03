# Projeto Studion

## Aula 4

Alguns dos conceitos estudados na **Aula-4**

```css
elemento {
  width: 100%; /* Esticar a imagem para ocupar todo o elemento onde está posicionada em largura */
  height: 100%; /* Esticar a imagem para ocupar todo o elemento onde está posicionada com altura */
  object-fit: cover; /* Faz com que a imagem envolva todo o elemento sem deformar */
  object-position: center; /* Centraliza a imagem */
  transition: 0.5s all ease; /* Cria uma animação de transição quando aplicar as modificações no :hover */
}
```

## Aula 5

Alguns conceitos estudados na **Aula-5**

## Trabalhando com grids

```html
<h3>
  Título 3
  <small>Texto para colocar embaixo do título</small>
</h3>
```

no css fica da seguinte forma:

```css
h3 small {
  display: block; /* Com isso, o que estiver dentro da tag <small> irá pra baixo do título */
}
```

```css
elemento {
  display: grid;
  grid-template-columns: repeat(3, minmax(300px, 1fr));
  place-items: center
    /* Funciona como justify-items:; e align-items:; em uma só propriedade */;
}
```

## Overflow e Auto-fill

Foi inserido a propriedade `overflow-x: hidden;` nos elementos `<header>`, `<main>`, `<footer>`:

```css
header,
main,
footer {
  overflow-x: hidden;
}
```

Essa propriedade impede que qualquer coisa saia de dentro dos blocos selecionados.

```css
.counter__container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  place-items: center;

  margin: 0;
  padding: 4.375rem 1rem;
}
```

## Estilizando a seção institutional

Alteração nos elementos da `<section class="institutional">`:

```html
<section class="institutional">
  <!-- Atribuído uma class no section institutional -->
  <!-- Elemento img movido para fora da DIV tornando elemento irmão de DIV -->
  <img
    class="institutional__image"
    src="./images/institutional.jpg"
    alt="Studion Institutional"
  />

  <!-- Inserido a class "Institutional__copy" -->
  <div class="institutional__copy">
    <h6>Fazemos o seu evento acontecer</h6>
    <h4>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</h4>

    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed, facere
      dolores? Aspernatur laboriosam molestiae a nisi odio cumque accusamus
      aliquid cupiditate rerum, officia quas aperiam nulla voluptates magni
      minus labore?
    </p>
    <!-- Inserido uma classe para o elemento button "btn btn-institutional" -->
    <button class="btn btn--institutional">Saiba Mais</button>
  </div>
</section>
```

E a estilização do html ficou assim:

```css
.institutional {
  display: grid; /* Definir elemento como grid container */
  grid-template-columns: auto auto; /* Duas colunas que se adaptam ao viewport automaticamente */
  gap: 3.125rem; /* Cria um espaçamento entre colunas */
  align-items: center; /* Alinhar div institutional ao centro verticalmente */
  padding: 4.375rem 1rem; /* Padding para definirmos o espaçamento interno do container */
}

.institutional__copy {
  padding: 0 1.875rem; /* Adição de espaçamento interno no bloco para os lados direito e esquerdo */
}
```
## CSS - Fonte secundária e estilizando o botão

```css
elemento {
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  /* 
    repeat(auto-fill, minmax(valorpx, valor fr) é bom usar pra quando quiser uma grid responsiva.
  */
}
```
## CSS - Estratégia de Container

Como delimitar o conteúdo dentro de um espaço conforme imagem do projeto
```css
.container { /* Classe utilitária para centralizar todo o site ao centro */
  max-width: 1140px; /* Significa que ele vai ter um tamanho máximo limitado. */
  margin: 0 auto; /* Irá alinhar a navbar ao centro da página */
}
```
## Medida ch
Uma medida excelente para trabalhar o kerning com o `letter-spacing: 1ch ou 0.5ch;`
### Ferramentas de Git
  [Commitizen](https://github.com/commitizen/cz-cli) - Ferramenta para formatar o texto do **commit**  

  Outra ferramenta para usar em conjunto

  [Commit-lint](https://github.com/conventional-changelog/commitlint) - Analiza o texto do commit, verifica se tem erros, ortografia.

  Também pode ser usado em conjunto com outra ferramenta  

  [Husky](https://github.com/typicode/husky)

### Cursos para aprender html e css gratuítos
 [codeacademy](https://www.codecademy.com/learn)

## Aula 6

### HTML - Revisando a estrutura do Quote

Adição da classe "quote" para colocar o background aplicando o efeito de paralax  
Adição da classe "container" para centralizar o conteúdo com a classe utilitária "container"  
Adição da classe "quote__copy" para editar o texto.
Adição da classe utilitária "copy--primary" na tag `<span>` para colorir o texto do span
Adição da classe base para o botão "btn"
Adição da classe modificadora do botão "btn--quote", classe específica para nossa seção "quote"
```html
<section class="quote">
  <div class="container quote__container">
    <div class="quote__copy">
      <h6>
        Você informa a temática e nós planejamos um evento com tecnologia e
      </h6>
      <h2><span class="copy--primary">Muito+ </span>Diversão</h2>
      <button class="btn btn--quote">Fazer cotação</button>
    </div>
  </div>
</section>
```

### CSS - Aplicando o efeito parallax

Começando a editar a seção "quote"

#### Efeito Paralax

Adicionamos a propriedade `background-image: url('./images/parallax.jpg');` para adicionar o Fundo.  
Adicionamos a propriedade `background-attachment: fixed;` para fixar o background.  
Adicionamos a propriedade `background-repeat: no-repeat;` para a imagem não se repetir.  
Adicionamos a propriedade `background-size: cover;` para a imagem ocupar a área inteira da class "quote".  
Adicionamos a propriedade `background-position: center;` para alinhar a imagem de fundo ao centro.  

```css
.quote {
  background-image: url('./images/parallax.jpg');
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
```
### CSS - Containers e Grids

Adicionamos uma cor de fundo a class "quote__copy".  
Adicionamos a propriedade `display: grid;` na class "quote__container", para tornar o elemento grid.  
Adicionamos a propriedade `align-items: center;` para alinhar o conteúdo da class "quote__container" centralizado verticalmente.  
Adicionamos a propriedade `min-height: 80vh;` para mostrar 80% da altura que o usuário consegue ver na tela. 

```css
.quote {
  display: grid;
  align-items: center;
  justify-items: end;
  min-height: 80vh;
}
.quote__container {
  display: grid;
  align-items: center;
  justify-items: center;
}
.quote__copy {
  background-color: #fff;
}
```
### CSS - Estilizando a caixa de texto

#### Estilizando a class "quote__copy"

Adicionamos a propriedade `padding: 5.625rem 4.375rem;` para adicionar espaçamento interno na caixa.  
```css
.quote__copy {
  background-color: #fff;
  padding: 5.625rem 4.375rem;
}
```

#### Estilizando o elemento "h6" dentro da classe "quote__copy"

Adicionamos a propriedade `font-weight: 400;` (Regular) ao nosso elemento h6.  
Adicionamos a propriedade `font-size: .9375rem;`  
Adicionamos a propriedade `letter-spacing: .1875rem;`  
Adicionamos a propriedade `line-height: 1.4375rem;`  
Adicionamos uma largura máxima limitado em carácteres com a propriedade definida em ch `max-width: 53ch;`    
Adicionamos a propriedade `text-transform: uppercase;` para estilizar as letras em caixa alta.  
Resetamos a margem com a propriedade `margin: 0;`.  

**Obs: O tamanho de um parágrafo que seria bom para leitura é em torno de 70/120 ch**
```css
.quote__copy h6 {
  font-size: .9375rem;
  font-weight: 400;
  letter-spacing: .1875rem;
  line-height: 1.4375rem;
  max-width: 53ch; /* Largura máxima limitado em caracteres */
  text-transform: uppercase;
  margin: 0;
}
```

#### Estilizando o elemento h2

Adicionamos a propriedade `font-size: 5rem;`.  
Adicionamos a propriedade `line-height: 5rem;` para colocar um espaço entre as linhas.  
Adicionamos a propriedade `text-transform: uppercase;`.  
Adicionamos a propriedade `letter-spacing: -.1875rem;`.
Adicionamos a propriedade `margin-top: 1.875rem;` para adicionar um espaço entre o h2 e h6.    
```css
.quote__copy h2 {
  font-size: 5rem;
  line-height: 5rem;
  text-transform: uppercase;
  letter-spacing: -.1875rem;
  margin-top: 1.875rem;

}
```

#### Estilizando o elemento span

Adicionamos a propriedade `display: block;`.  
```css
.quote__copy h2 span {
  display: block;
}
```
### CSS - Estilizando o botão e Finalizando o Quote

#### Estilizando a class "btn__quote"

Adicionamos a propriedade `color: var(--color-copy);`.  
Adicionamos a propriedade `border-color: var(--color-copy);`  
Adicionamos a propriedade `background: unset;` que retira o fundo do elemento.  

```css
.btn--quote {
  color: var(--color-copy);
  border-color: var(--color-copy);
  background: unset;
}
```

#### Alteração da margem do h2

```css
.quote__copy h2 {
  font-size: 5rem;
  line-height: 5rem;
  text-transform: uppercase;
  letter-spacing: -.1875rem;
  margin: 1.875rem 0;
}
```
# Aula 7 - Site de Eventos: Finalizando a Home com o Footer

## CSS - [Font Awesome](https://fontawesome.com/)

Adicionamos os imports no começo do **CSS**
```css
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.14.0/css/fontawesome.min.css');
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.14.0/css/brands.min.css');
```

Adicionamos os ícones de rede social no html da seguinte forma:  
```html
<ul>
  <li>
    <a href="https://www.facebook.com/" target="_blank">
      <i class="fab fa-facebook fa-2x"></i>
    </a>
  </li>
  <li>
    <a href="https://twitter.com/" target="_blank">
      <span class="fa-stack">
        <i class="fas fa-circle fa-stack-2x fa-inverse"></i>
        <i class="fab fa-twitter fa-stack-1x"></i>
      </span>
    </a>
  </li>
  <li>
    <a href="https://www.youtube.com/" target="_blank">
        <i class="far fa-play-circle fa-2x"></i>
    </a>
  </li>
</ul>
```
## HTML e CSS - Estrutura, container e grid

#### Alterações no HTML:
- Adicionamos uma classe no elemento `<footer>` com o nome "footer".
- Adicionamos uma classe no elemento `<h2>` com o nome "logo-studion".
- Adicionamos uma classe no primeiro elemento `<span>` com o nome "copy--primary".
- Adicionamos uma classe no segundo elemento `<span>` com o nome "logo-studion__subtitle".
- Organizamos o conteúdo da logo.
- Adicionamos uma div com as classes: "container" e "footer__container"
- Colocamos o conteúdo do elemento `<h2>` até a lista dentro da div com as duas classes
```html
<footer class="footer">
  <div class="container footer__container">
    <h2 class="logo-studion">
      Studi<span>on</span>
      <span class="logo-studion__subtitle">Eventos</span>
    </h2>
    <form class="footer__form" action="">
      <label for="">receba news e promoções</label>
      <input type="email" placeholder="email" />
      <button type="submit">Enviar</button>
    </form>
    <ul class="footer__social">
      <li>
        <a href="https://www.facebook.com/" target="_blank">
          <i class="fab fa-facebook fa-2x"></i>
        </a>
      </li>
      <li>
        <a href="https://twitter.com/" target="_blank">
          <span class="fa-stack">
            <i class="fas fa-circle fa-stack-2x fa-inverse"></i>
            <i class="fab fa-twitter fa-stack-1x"></i>
          </span>
        </a>
      </li>
      <li>
        <a href="https://www.youtube.com/" target="_blank">
          <i class="far fa-play-circle fa-2x"></i>
        </a>
      </li>
    </ul>
  </div>
  <hr />
  <p>
    <small>Studi<span>ON</span> - Todos os direitos reservados</small>
  <p>
</footer>
```
#### Footer - Formulário
- Adicionamos uma classe no elemento `<form>` com o nome "footer__form".
```html
  <form class="footer__form" action="">
  </form>
```
#### Footer - Lista
- Adicionamos uma classe no elemento `<ul>` com o nome "footer__social".
```html
<ul class="footer__social">
</ul>
```
## Estilizando a class ".footer"
- Adicionamos uma cor de fundo preto `background-color: #000;`
- Adicionamos uma cor para o texto `color: #fff;`
- Adicionamos um padding nas laterais para criar um espaço interno no elemento.
```css
.footer {
  background-color: #000;
  color: #fff;
  padding: 0 1rem;
}
```
## Estilizando a class ".footer__container"
- Adicionamos a propriedade `display: grid;` para tornar o elemento como grid.
- Adicionamos a propriedade `grid-template-columns: repeat(3, auto);` para as colunas do nosso grid.
- Adicionamos a propriedade `align-items: center;` para alinhar os elementos verticalmente.
```css
.footer__container {
  display: grid;
  grid-template-columns: repeat(3, auto);
  align-items: center;
}
```
## Estilizando a class ".logo-studion"
- Adicionamos a propriedade `justify-self: start;` para alinhamento.
```css
.footer .logo-studion {
  justify-self: start;
}
```

## Estilizando a class ".logo-studion__subtitle"
- Adicionamos a propriedade `display: block;` para quebrar a linha na logo studion do footer.
```css
.logo-studion__subtitle {
  display: block;
}
```

## Estilizando a class ".footer__form"
- Adicionamos a propriedade `justify-self: center;` para alinhamento ao centro.
```css
.footer__form {
  justify-self: center;
}
```

## Estilizando a class ".footer__social"
- Adicionamos a propriedade `justify-self: end;` para colocar no final.

```css
.footer__social {
  justify-self: end;
}
```
## CSS - Margens e Formulário

- Alteramos a classe ".logo__studion" para retirar a margem da logo.
- Adicionamos um espaço interno na classe ".footer__container" para o conteúdo não ficar muito colado na borda do elemento footer.
`grid-template-columns: 5.625rem auto;`
```css
.footer .logo-studion {
  justify-self: start;
  margin: 0;
}
.footer .footer__container {
  display: grid;
  grid-template-columns: repeat(3, auto);
  align-items: center;
  padding: 5.25rem 0;
}
```
- Adicionamos as propriedades na classe ".footer__form" definindo a classe como grid
- Adicionamos duas colunas na classe ".footer__form" com a propriedade 
- `gap: 1.25rem;` para adicionar um espaço entre o elemento `<label></label>` e o elemento irmão, `<fieldset></fieldset>`.
```css
.footer__form {
  display: grid;
  place-items: center;
  grid-template-columns: 10ch auto;
  gap: 1.25rem;
}
```
Adicionamos algumas propriedades no elemento `<fieldset></fieldset>`:  
- `border: unset;` para retirar os valores de borda.
- `margin: 0;` para retirar os valores de margem.
- `padding: 0;` para retirar os valores de padding do elemento.
- `width: 100%;` para o nosso `<fieldset></fieldset>` ocupar todo espaço disponível da coluna

```css
.footer__form fieldset {
  border: unset;
  margin: 0;
  padding: 0;
  width: 100%;
}
```
- Adicionamos o elemento html `<fieldset></fieldset>` para agrupar dois elementos dentro da tag ".footer__form" conforme abaixo.
- Adicionamos uma "id" no elemento `<input id="email" />` para interligar com o elemento `<label for="email"></label>` onde adicionamos um atributo "for".

```html
<label for="email">receba news e promoções</label>
<fieldset>
  <input id="email" type="email" placeholder="email" />
  <button type="submit">Enviar</button>
</fieldset>
```
### .footer__form label

```css
.footer__form  label {
  
}
```

### .footer__form input
- `width: 100%;` para nosso input ocupar a largura total do espaço disponível  da coluna.

```css
.footer__form input {
  width: 100%;
}
```