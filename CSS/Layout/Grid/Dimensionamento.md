# Dimensionamento

- Formas de dimensionar a grade.

## Dimensionamento intrínsico

- Depende apenas do próprio elemento
- Palavras-chaves/Funções:
  - `min-content`: O tamanho será o menor tamanho sem que ocorra um overflow
  - `max-content`: O tamanho será o tamanho do conteúdo se disposto numa linha infinita, sem que ocorra quebras de linhas.
  - `fit-content(tamanho)`:
    - Agirá como `max-content` se for menor que `tamanho`. Caso contrário, será `tamanho`.
    - `=min(max-content, tamanho)`
    - Por exemplo, digamos que tenhamos caixas que devem ter no máximo 300px. E queremos que as caixas menores que 300px, tenham o tamanho do seu conteúdo.
  - `fit-content`: Usa o espaço disponível, mas nunca menos que `min-content` e não mais que `max-content`.
  - `auto`: Ao utilizar esta palavra-chave para dimensionar tracks, as tracks irão preencher todo o container. Irão usar o espaço disponível, mas tem menor precedência que as unidades `fr`

## Unidade fr

- A unidade `fr` representa uma fração/parte do espaço disponível.
- Valores diferentes para `fr` distribuirão o espaço disponível em proporção.

## Função minmax

- Recebe dois tamanhos como parâmetros, e faz com que a track não tenha um tamanho menor que o primeiro tamanho especificado e nem maior que o último parâmetro especificado.

## Notação repeat

- Repete uma seção da listagem de tracks.
- No primeiro parâmetro:
  - `auto-fill`: Criará tantas colunas quantas podem caber no container.
  - `auto-fit`: Igual, mas as colunas irão começar a se expandir caso haja trilhas vazias. As trilhas vazias colapsarão para 0.