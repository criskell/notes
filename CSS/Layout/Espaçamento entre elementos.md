# Espaçamento

- Técnicas de espaçamento entre elementos:
  - margin
  - gap
  - padding
  - propriedades de deslocamento



## margin

- Cria um espaçamento externo ao elemento

- Shorthand para outras props.

- Sintaxe:

  - ```css
    /* 1 valor - margens iguais para todos os lados */
    margin: 10px;
    /* 2 valores - <lado superior e inferior: 20px> <lado esquerdo e direito: 30px> */
    margin: 20px 30px;
    /* 3 valores - <lado superior: 20px> <lado esquerdo e direito: 50px> <lado inferior: 30px> */
    margin: 20px 50px 30px;
    /* 4 valores - <lado superior: 10px> <lado direito: 20px> <lado inferior: 30px> <lado esquerdo: 40px> */
    margin: 10px 20px 30px 40px;
    ```

- Valores:

  - `auto`:
    - Em elementos **block-level** com dimensionamento **extrínseco**, pega o espaço disponível na direção em que é aplicada
  - `%`: Obtém o valor computado relativo à largura do containing block
  - `<length>`

- Margens na direção do bloco colapsam

- Margens negativas **reduzem** o espaçamento entre um elemento, ao contrário de margens positivas, que adicionam espaçamento

## padding

- Cria espaçamento na parte interna
- Pode afetar as dimensões da caixa
- Propriedade `padding` é um shorthand para `padding-[top, right, bottom, left]`



## propriedades de deslocamento

- `top`, `right`, `bottom`, `left`
- Elementos posicionados
  - `relative`: Relativo ao próprio elemento
  - `absolute`: Relativo ao containing block/contexto de posicionamento
  - `fixed`: Relativo à viewport
  - `sticky`: Somente funcionará quando tiver em um estado "preso"



## gap

- É utilizado para criar uma lacuna **entre** elementos filhos de um container flex ou grid
- Shorthand para as propriedades `row-gap` e `column-gap`



## espaçamento consistente

- escolha uma técnica
- utilize apenas uma medida de espaçamento **consistente** entre elementos
- utilize `em` para separação vertical que se baseará no `font-size` do próprio elemento
- lacunas entre elementos na *mesma linha* são conhecidos como *gutters*