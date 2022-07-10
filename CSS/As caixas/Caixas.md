# Caixas

- São caixas retangulares geradas para cada elemento.
- Podemos dividir em 4 partes circundantes, de fora para dentro:
  - Margem: A margem separa a caixa de outros elementos.
  - Borda: A **borda** da caixa. Define os limites da caixa.
  - Preenchimento: O preenchimento é o espaçamento interno da caixa ao longo da borda
  - Conteúdo: Parte onde fica o conteúdo

## Margem

- Separa a caixa de seus elementos irmãos.
- A margem não afeta o tamanho da caixa e sim o que há ao redor.
- Cerca a *edge* da borda de uma caixa.
- Propriedades:
  - `margin` + longhands: Define a espessura da área de margem


## Borda

- Define os limites de uma caixa visualmente
- Cada borda tem:
  - espessura (`border-width`)
  - cor (`border-color`)
  - estilo (`border-style`)
- Shorthand
  - `border-width border-style [border-color]`
- É adicionado às dimensões da caixa, por padrão

## Preenchimento

- É o espaçamento ao redor da borda e conteúdo
- É inserido entre a *edge* de preenchimento e a *edge* de conteúdo
- Fica *dentro* da caixa e é transparente, portanto, é afetado por props. como `background`
- Propriedades:
  - `padding`: Define a espessura da área de preenchimento.


## Conteúdo

- A área de conteúdo é onde fica o conteúdo real

