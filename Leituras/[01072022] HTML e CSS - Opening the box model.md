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
- Parei no "So far a lot of these properties might not make a whole lot of sense, and that’s all right. To clarify things, let’s take a close look at all of the properties—`width`, `height`, `padding`, `border`, and `margin`—that go into forming the box model."