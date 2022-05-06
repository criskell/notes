# Valores e unidades

- Um tipo de valor (ou tipo de dados) é uma coleção de valores permitidos.
- Notação: `<tipo-de-valor>`, por exemplo `<color>`.

## Tipos numéricos

- `<integer>`: Número inteiro sem componente fracionário.
- `<number>`: Número que pode ter um componente fracionário.
- `<dimension>`: `<number><unidade>`, exemplo `10.5px`
- `<percentage>`: Número que indica uma fração em relação a outro valor.

### Comprimentos

- Tipo `length`
- São `<dimension>` que referem-se a distâncias.
- Tipo de unidade de comprimento:
  - Absoluto: Não é relativo.
  - Relativo: É relativo a outro valor.
    - `em`: Relativo a fonte do elemento pai (no caso em um contexto tipográfico) ou relativo ao tamanho da fonte do próprio elemento em outros casos. Exemplo: `1.5em`, ou seja, 1.5 vezes o tamanho da fonte do elemento pai.
    - `rem`: Relativo a fonte do elemento raiz.

### Porcentagens

- Indica uma fração em relação a outro valor.

## Cor

- Formas para especificar cores:
  - Palavra-chaves como `yellow`
  - Códigos hexadecimais: Começa com `#`, e é seguido por 6 ou 8 algarismos hexadecimais. Cada par de algarismo representa um canal de cor (vermelho, verde e azul) que pode assumir 256 valores diferentes.
  - RGB ou RGBA: Um valor RGB assume a forma de função `rgb(decimalVermelho, decimalVerde, decimalAzul)`. Um valor RGBA assume a forma de função `rgba(vermelho, verde, azul, opacidade)` igual ao `rgb` mas aceita um outro valor que indica a opacidade da cor (canal alfa) entre 0 e 1.
  - HSL ou HSLA: Assuma a forma `hsl(matiz: tom base da cor, saturação: 0 até 100%, luminosidade: 0 até 100%)`. HSLA para indicar o canal alfa.

## Imagens

- O tipo `<image>` representa imagens, como imagens externas ou gradientes.

## Posições

- O tipo `<position>` denota coordenadas bidimensionais.

## Strings e identificadores

- Strings são delimitadas por aspas e identificadores não.
- `yellow` é um identificador.

## Notação funcional

- Functional notation é um tipo de valor que pode representar tipos mais complexos.