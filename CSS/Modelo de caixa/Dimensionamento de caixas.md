## Dimensionamento de caixas

- Tamanho total:
  - todas as propriedades do modelo de caixa, incluindo margem, somadas
  - altura e largura
- Se `box-sizing: border-box`, então a largura total será `margin-left + margin-right + width`. Se forem adicionadas bordas e preenchimentos, a área de conteúdo será diminuida 

- No caso de caixas em nível de bloco:

  - Com o posicionamento não absoluto, não esticado e muito menos fixo, a caixa irá ocupar todo o pai, e as bordas e preenchimentos serão empurradas para dentro.

  - Com `100%` de largura definida explicitamente, a caixa irá vazar do seu pai, se houver preenchimentos ou bordas.

  - Com `position == absolute`, o dimensionamento é intrínsico

## Larguras e alturas máximas e mínimas

- Permite adicionar uma largura/altura máxima até onde o elemento pode se expandir
- Ou uma largura/altura mínima até onde o elemento pode encolher

## Alturas

- Propriedade `height`
- Valores:
  - Porcentagens:
    - irá se referir a altura do containing block, que muitas vezes é baseado na altura dos filhos. ou seja, irá ser uma definição circular e não funcionará.
- Dicas:
  - evite alterar a altura de um elemento

## Box-sizing

- Controla o dimensionamento das caixas.
- Modelo de caixa padrão:
  - as propriedades `width/height` dimensionam o conteúdo e não o elemento como um todo
  - bordas e preenchimentos são somadas a largura e altura e aumentam as dimensões do elemento
- `content-box`:
  
  - `width` e `height` controla a **caixa de conteúdo**
  - A largura total da caixa é conteúdo + preenchimento + borda e a mesma coisa pra altura.
  - podemos pensar que ao adicionar `padding || border` numa caixa com dimensionamento extrínsico, irá esticar a caixa para além da largura/altura especificada
  - a largura/altura inclui apenas o conteúdo 
  - padding + border são adicionadas ao tamanho inicial.
  - 
- `border-box`:
  
  - `width` e `height` controla o tamanho da caixa visível (da borda até o conteúdo).
  - A largura total é especificada pelo `width` e altura pelo `height`.
  - a largura/altura inclui conteudo + border + padding
  - resulta no padding + border diminuindo o conteúdo a partir do tamanho definido
  - padding e height passam a não aumentar a largura total da caixa
  - Isso incluirá todas as bordas e preenchimentos nas dimensões originais que você definiu.
  
  

## Tipos de dimensionamento

- Extrínsico:
  - A caixa tem dimensões fixas controladas pelo autor
  - Há um limite de quanto conteúdo pode adicionar antes saia dos limites da caixa
- Intrísinco:
  - A caixa é dimensionada de acordo com a quantidade de conteúdo