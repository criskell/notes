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

## Box-sizing

- Controla o dimensionamento das caixas.
- `content-box`:
  - padding + border são adicionadas ao tamanho inicial.
- `border-box`:
  - padding + borders empurram o conteúdo a partir do tamanho definido
