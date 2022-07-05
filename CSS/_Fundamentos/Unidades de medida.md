# Unidades de medida

## Tipos de unidades

- Absoluta:
  - Nenhum fator é considerado para computar o valor final.
- Relativa:
  - Fatores são considerados para computar o valor final.

## Números

- Números podem ser inteiros sem unidades e decimais (0.1, 0.2, etc.).

## Porcentagens

- Frações que se referem a outro valor.
- Ao que é referido:
  - Na propriedade `width`, `margin` e `padding`: Na largura do container pai.
  - Na função `transform`: É referido a largura do elemento.

## Dimensões e comprimentos

- Dimensões: Números (ou seja, tipo `<number>`) + Unidade. Exemplos: `10rem`.
- Comprimentos: Dimensões que referem-se a distâncias.
  - Tipos:
    - Absolutos: São comprimentos por si só.
    - Relativos: É calculado em relação a um valor base que pode mudar.
    - As unidades absolutas são comparadas com um valor base que não pode mudar e unidades relativas são comparadas com um valor base que pode mudar.
  - Unidades absolutas de comprimento:
    - `pt`: não é recomendado para uso em tela
  - Unidades relativas de comprimento:
    - Unidades relativas a fontes:
      - `em`:
        - Relativo ao tamanho computado da fonte do elemento pai ou do elemento atual.
        - Utilizar esta unidade no preenchimento e margem ajuda a manter um ritmo vertical, pois ao redimensionar a fonte, é dimensionada proporcionalmente
      - `rem`:
        - Relativo ao tamanho da fonte do elemento raíz.
      - `ch`:
        - Relativo ao tamanho do caractere '0'.
    - Unidades relativas a viewport:
      - `vw`: 1% da largura da viewport.
      - `vh`: 1% da altura da viewport.

## Outras unidades

- Unidades de ângulos:
  - Útil para definir valores de graus.
  - `1turn` = `360deg`

## Perguntas de revisão

1. O que são dimensões.
2. O que são comprimentos.
3. O que é utilizado no cálculo de porcentagens nas propriedades `width`, `padding` e `margin` e na função `transform`.