# Unidades de medida

## Tipos de unidades

- Absoluta:
  - O seu valor base não muda
  - Nenhum fator é considerado para computar o valor final.
- Relativa:
  - Relativo a um valor base que pode mudar
  - Fatores são considerados para computar o valor final.
- As unidades absolutas são comparadas com um valor base compartilhado que não pode mudar e unidades relativas são comparadas com um valor base que pode mudar.

## Unidades de comprimento

## Unidades absolutas

- px:
  - Unidade de pixeis
  - Obs.: Não é exatamente pixeis


### Unidades relativas

- Unidades relativas a fontes:
  - `em`:
    - Relativo ao tamanho computado da fonte do elemento pai (em um contexto tipográfico, por exemplo `font-size`) ou
    - relativo ao tamanho da fonte do próprio elemento em outros casos (como a propriedade `width`).
    - ou seja: o que tiver mais perto.
    - Exemplo: `1.5em`, ou seja, 1.5 vezes o tamanho da fonte do elemento pai.
  - `rem`:
    - Relativo ao tamanho da fonte do elemento raíz.
  - `ex`:
    - Tamanho da altura x.
  - `ch`:
    - Largura do caractere 0.
- Unidades relativas a viewport:
  - `vw`: 1% da largura da viewport.
  - `vh`: 1% da altura da viewport.

## Unidades de ângulos

- Útil para definir valores de graus.
- `1turn` = `360deg`

## Perguntas de revisão

1. O que é utilizado no cálculo de porcentagens nas propriedades `width`, `padding` e `margin` e na função `transform`.

## Dúvidas

1. Um pixel é mesmo um pixel em qualquer circunstância?