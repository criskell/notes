# Modelo de caixas

- Modelo de caixas diz que todo elemento é representado como uma caixa e define regras de interação entre elas.
- Cada caixa tem um tipo de exibição:
  - Externa: Controla a disposição ao redor do elemento.
  - Interna: Controla a disposição dos elementos filhos.

## Exibição externa

- Tipo bloco:
    - Cria uma nova linha.
    - Ocupa todo o espaço do elemento pai.
    - `width` e `height` aplicados.
    - margens, bordas e preenchimentos são aplicados e faz outros elementos se moverem.

- Tipo em linha:
    - Não cria uma nova linha.
    - Ocupa o espaço necessário.
    - `width` e `height` não aplicados.
    - margens, bordas e preenchimentos horizontais são aplicados e faz outros elementos se moverem.
    - margens, bordas e preenchimentos verticais são aplicados e não faz outros elementos se moverem.


## Anatomia de uma caixa

- Cada caixa irá ser composta por 4 áreas:
  - Conteúdo: Armazena o conteúdo.
  - Preenchimento: Envolve a área de conteúdo.
  - Borda: Circunda a área de preenchimento e define os limites da caixa.
  - Margem: Envolve a área de borda e define o espaço externo desta caixa dentre os elementos que estão perto da caixa.


## Dimensionamento

- Dimensionamento extrínsico é quando a caixa possui uma largura e altura definida e um limite de conteúdo antes que o conteúdo transborde para fora da caixa.
- Dimensionamento intrínsico de uma caixa é o dimensionamento feito de acordo com o conteúdo dela.
- Overflow ocorre quando o conteúdo da caixa ultrapassa os limites dela.

## Controlando o tamanho total de caixas

- `box-sizing: content-box` (este é o modelo de caixa padrão):
  - `width` e `height` controla a **caixa de conteúdo**.
  - A largura total da caixa é conteúdo + preenchimento + borda e a mesma coisa pra altura.
  - podemos pensar que ao adicionar `padding || border` numa caixa com dimensionamento extrínsico, irá esticar a caixa para além da largura/altura especificada
- `box-sizing: border-box `(este é o modelo de caixa alternativo):
  - `width` e `height` controla o tamanho da caixa visível (da borda até o conteúdo).
  - A largura total é especificada pelo `width` e altura pelo `height`.
  - padding e height passam a não aumentar a largura total da caixa

## Colapso de margem

- É a junção de duas margens superiores e inferiores em apenas uma.
- Acontece quando as margens se tocam.
- Se ambas forem positivas, o tamanho total da margem é o maior tamanho entre as margens.
- Se uma for negativa, o tamanho total da margem é igual a margem positiva subtraída a margem negativa.
- Se ambas forem negativas, o tamanho total será a margem menor (ou seja, a mais distante do zero).

## Caixas genéricas

- `div`
- `span`

## Caixas do tipo inline-block

- Tem características inline e block. Um meio-termo, por exemplo, respeita width e height.
