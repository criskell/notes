# Imagens responsivas

- Imagens responsivas são imagens que se adaptam para diferentes tamanhos de tela, resoluções e etc.

## Vantagens

- Resolver problemas como:
  - Problema direção de arte:
    - Necessidade de servir diferentes imagens **adaptadas** para diferentes resoluções de telas.
    - Por exemplo: Digamos que tenhamos uma imagem muito grande, com vários detalhes, e em telas pequenas desejamos exibir uma pequena imagem com os detalhes importantes desta imagem.
  - Problema de troca de resolução:
    - Necessidade de servir imagens de **tamanhos** diferentes para diferentes resoluções de telas.
    - Por exemplo:
      - Digamos que tenhamos uma imagem muito grande de 1000px / 1000px
      - Em telas menores, não precisamos exibir esta imagem muito grande.
      - Agora e se tivermos uma imagem de 100 x 100?
      - Em telas maiores, talvez queremos exibir estas imagens maiores, e isso ficaria muito borrado, os pixeis ficariam mais "grandes". A não ser que utilizamos imagens vetoriais, que são diferentes de imagens raster.
  - Usuários de dispositivos móveis preferem não gastar largura de banda.
  - Já usuários com telas maiores irão necessitar de imagens maiores para exibir com mais detalhes.

-  Podemos resolver estes problemas servindo diferentes versões da imagem, com:
  - alternância de resolução: Alterar a largura e altura
  - direção de arte: uma imagem adaptada melhor para o contexto atual.
- Mas como?
  - `picture`
  - `srcset`

## Resolution switching

- Necessidade de servir imagens menores para telas menores ou o inverso. Além disso, exibir imagens com diferentes resoluções dependendo da densidade de pixels.
- Resolvemos este problema com o atributos `srcset` e `sizes` ou ainda, SVG.

### Diferentes tamanhos

### Mesmos tamanhos, mas diferentes resoluções

## Art direction

- Necessidade de servir imagens adaptadas (cortadas) ao contexto atual.
- Resolvemos este problema com o elemento `picture`.