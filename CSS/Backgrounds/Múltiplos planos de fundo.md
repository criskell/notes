# Múltiplos planos de fundo

- É possível utilizar múltiplos planos de fundos nas propriedades `background-*` através de uma lista.
- Os planos de fundos listados são empilhados, onde a parte superior é o primeiro fundo especificado e a parte inferior é o último fundo especificado.
- Apenas o último plano de fundo pode incluir uma cor.

## Exercícios

1. Podemos utilizar várias imagens na propriedade `background-image` através de uma lista separada por vírgulas. Como se dá o empilhamento de imagens? Qual aparece no topo de todas as imagens e qual imagem aparece no fundo de toda a pilha de imagens?
2. Dado as declarações `background-image: url(URL-da-imagem.jpg), #fff` e `background-image: #fff, url(URL-da-imagem.jpg)`, me diga: qual é a correta?