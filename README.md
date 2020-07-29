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
Adicionamos a propriedade `background-attachment: fixed;` que já traz um efeito paralax   
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