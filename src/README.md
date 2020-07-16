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

### Trabalhando com grids

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

### Overflow e Auto-fill

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
