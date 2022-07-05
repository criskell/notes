# Leitura: Opening the box model

- Link: https://learn.shayhowe.com/html-css/opening-the-box-model/
- Data: 01/07/2022

## Como os elementos são exibidos

- Podem serem exibidos como:
  - Elemento de nível de bloco:
    - Ocupam toda o espaço horizontal **disponível**
    - Criam novas linhas
    - São elementos para maiores partes do conteúdo
  - Elemento de nível em linha:
    - Ocupam o espaço necessário para o seu conteúdo
    - Se alinham na mesma linha
    - São elementos para pequenas partes do conteúdo

## Propriedade display

- Determina como o elemento é exibido, em nível de bloco, inline, etc.
- `inline-block`: fará que se comporte como um elemento em nível de bloco, podendo receber as propriedades do modelo de caixa, e irá se alinhar na mesma linha

## O modelo de caixa

- Cada elemento na página é uma caixa.
- O núcleo da caixa é determinado pela altura e largura de um elemento, determinado `width` / `height`, conteúdo ou `display`
- O preenchimento e as bordas estendem as dimensões da caixa para fora da largura e altura do elemento
- O modelo de caixa padrão é aditivo, assim para determinar o tamanho real da nossa caixa levamos em consideração o preenchimento, as bordas e as margens.

## Largura e altura

- Cada elemento possui uma largura e altura padrão
- A largura padrão depende do `display`
- A altura padrão de um elemento depende de seu conteúdo

## Margens e preenchimento

- Margens:
  - É o espaço ao redor de um elemento
  - Está *fora* de um elemento
  - É transparente
  - Casos de uso:
    - Para fazer elementos respirarem
    - Para posicionamento
- Preenchimento:
  - É o espaço entre a borda e conteúdo
  - Está dentro de um elemento
  - É transparente
- No caso de inline-level,
  - as margens e preenchimentos horizontais são aplicadas e afastam os elementos
  - os preenchimentos verticais possuem um efeito visível na tela, mas não afastam outros elementos, podendo sobrepor a outros elementos
  - margens verticais não funcionam

## Bordas

- Delimitam um elemento
- Cada borda possui
  - largura
  - estilo
  - cor
- Shorthand `border: largura estilo cor`, mesma sintaxe para `border-[top|right|bottom|left]`
- Podemos ser mais específicos, utilizando `-style`, `-width` ou `-color`

### Raio da borda

- `border-radius`: cantos de um elemento arredondados

- identifica o raio de arredondamento em cada canto

- sintaxe:

  - ```css
    border-radius: <todos os lados>;
    border-radius: <top-left + bottom-right> <top-right bottom-left>
    border-radius: <top-left> <top-right> <bottom-right> <bottom-left>
    ```

- Longhands:

  - `border-[top|bottom]-[left|right]-radius`