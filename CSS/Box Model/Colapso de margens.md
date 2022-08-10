# Colapso de margens

- Colapso de margem ocorre quando duas margens (verticais) que se tocam são colapsadas/recolhidas/combinadas em **apenas uma**
- Tamanho da margem:
  - Se ambas forem positivas, `max(margin_1, margin_2)`,
  - Se ambas forem negativas, `min(margin_1, margin_2)`,
  - Caso contrário, `margin_1 + margin_2`
- Casos:
  - Irmãos adjacentes:
    - Entre caixas que são irmãs adjacentes
    - Exceto:
      - se a última não está sendo limpa
      - se não é uma caixa em nível de bloco
  - Descendentes e a caixa pai sem separação:
    - Se não houver separação entre a descendente e a pai, haverá colapso
    - `margin-top` de descendentes são colapsadas com `margin-top` do pai, se não houver `border`, `padding`, conteúdo inline, BFCs e limpeza de floats os separando.
    - `margin-bottom` de descendentes são colapsadas com `margin-bottom` do pai se não houver `border`, `padding`, conteúdo inline, `min-/height` os separando.
    - Margens sempre tentam aumentar a distância entre irmãos (diferente do `padding`, que pode ser utilizado para aumentar a lacuna entre pai/filho). Mesmo que isso signifique ser transferida (e recolhida) para o pai, em algumas condições
    - A margem fica fora da caixa pai.
    - Exceto:
      - floats
      - elementos absolutamente posicionados
      - inline-block
      - overflow
  - Caixas vazias:
    - Se não houver `border`, `padding`, conteúdo inline, alturas, separando a `margin-top` da `margin-bottom` de seu pai, são colapsadas.
  - Somente margens verticais são colapsadas.
  - Margens zero são colapsadas.

## Exercícios

1. O que é colapso de margens?
2. Quais são os casos em que margens serão colapsadas?
3. Cite algumas caixas que nunca terão margens colapsadas.