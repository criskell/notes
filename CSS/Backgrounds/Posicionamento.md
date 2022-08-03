# Posicionamento de planos de fundo

- A propriedade `background-position` especifica o posicionamento de um plano de fundo na caixa.
- Valores:
  - Comprimentos:
    - Especifica a distância do *top left* do elemento do *top left* do plano de fundo.
  - Porcentagens:
    - Dado um posicionamento `X%`, moverá um ponto com origem no topo superior esquerdo da imagem localizado em `X%` para um ponto no container com origem no topo superior esquerdo do container localizado em `X%` no container. Alinhará o ponto `X%` da imagem ao ponto `X%` do container.
    - O valor de uma porcentagem é relativo ao cálculo: `box size - image size`
  - `keyword`:
    - `top`: 0% verticalmente
    - `left`: 0% horizontalmente
    - `right`: 100% horizontalmente
    - `bottom`: 100% verticalmente
- Sintaxes:
  - Um valor: O primeiro valor é o deslocamento horizontal e o deslocamento vertical é `center`.
  - Dois valores:
    - O primeiro valor é o deslocamento horizontal e o segundo valor é o deslocamento vertical.
    - Se informado o valor horizontal, `center` atua como o valor vertical e vice-versa.
  - Três valores / Quatro valores:
    - Este tipo de sintaxe permite especificar a distância que o plano de fundo deve ter de lados especificados.
    - Permite posicionar uma imagem a partir de outro ponto além do `top left`
    - Não aceita `center`
    - Um valor de comprimento ou porcentagem deve seguir uma palavra-chave e indica uma distância da borda da palavra-chave

## Exercícios

1. Como alterar o posicionamento de um plano de fundo num elemento?
2. Qual é a origem de um posicionamento feito com valores do tipo comprimento e a distância desta origem será para qual ponto do plano de fundo?
3. Se eu alterar o posicionamento do plano de fundo no eixo X para `50%` é correto afirmar que o canto superior esquerdo do plano de fundo será deslocado 50% relativo ao canto superior esquerdo do elemento?
4. Converta os valores de palavra-chave para porcentagens.
5. O que acontece se eu fornecer apenas um valor para o posicionamento?
6. E se eu fornecer dois valores?
7. `top left` é a mesma coisa que `left top`? Ou seja, a ordem quando somente há palavras-chaves não importa?
8. O que acontece se eu fornecer `left center` ou `center left`? É  a mesma coisa? Para qual eixo o `center` é aplicado nestes dois casos?
9. Como funciona a sintaxe de três a quatro valores? O que permite fazer? O que acontece se eu não fornecer um deslocamento?
10. As porcentagens na propriedade `background-position` referem-se ao qual valor?