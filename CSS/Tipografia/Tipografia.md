# Tipografia

## Fontes

- Alterar tipo de letra:
  - `font-family`
  - Fontes específicas: Entre aspas
  - Fontes genéricas: Palavras-chaves
  - O navegador irá escolher a primeira fonte na lista que está disponível para baixar e que suporta os caracteres atuais da página
- Itálico:
  - `font-style`, aceita
  - `italic`: uma versão cursiva do tipo de letra normal
  - `oblique`: uma versão inclinada do tipo de letra normal
  - `normal`
- Negrito:
  - `font-weight`
  - aceita `bold`, `normal` que equivalem, respectivamente, à `700` e `400`
  - aceita palavras-chaves relativas ao pai, como `bolder` e `lighter`
  - ou valores numéricos, como `100-900` (ou seja, na casa dos 100, para fontes *não variáveis*)
- Dimensionamento das fontes:
  - `font-size`
  - aceita `<length-percentage>` ou palavras-chaves
  - palavras-chaves absolutas como `medium`, `small` e `large`
  - palavras-chaves relativas ao tamanho da fonte no pai do elemento, como `larger` e `smaller`
- Transformação de texto
  - `text-transform`
  - `uppercase`
  - `lowercase`
  - `capitalize`
  - `full-width`
- `text-decoration`
  - shorthand
  - `text-decoration-thickness`: altera a largura do traço das decorações
  - `text-decoration-position`: especifica o deslocamento apenas da linha `underline`
- `font-variant`:
  - Shorthand para propriedades que permitem habilitar variantes da fonte como `small-caps` e `slashed-zero`

## Layout de texto

- Altura das linhas:
  - `line-height`
  - comprimentos, porcentagens ou `<number>`
  - especifica a altura das linhas do elemento
- Espaçamento entre letras:
  - `letter-spacing`
  - Controla o espaçamento entre letras
  - Aumenta ou diminui a quantidade de espaçamento natural entre letras
- Espaçamento entre palavras:
  - `word-spacing`
  - Controla o espaçamento entre palavras
  - Aumenta ou diminui a quantidade de espaçamento natural entre palavras.
  - É um espaçamento extra além do normal: `word-spacing: 0 == word-spacing: normal`
- Recuo
  - `text-indent`
  - Adiciona um recuo na primeira linha
- Estouro de texto
  - `text-overflow`
  - Controla como o conteúdo de texto escondido devido ao `overflow: hidden` deve ser apresentado
  - `clip` (padrão): o conteúdo é recortado
  - `ellipsis`: uma reticências é mostrada no ponto de estouro
- Controlando o espaço em branco:
  - `white-space`
  - Especifica como o espaço em branco de um texto deve ser tratado
- Quebra de palavras no texto:
  - `word-break`
  - Especifica se uma palavra deve ser quebrada ao transbordar de uma linha
  - `normal`: a palavra não é quebrada
  - `break-all`: a palavra é quebrada sempre que transborda
- Alinhamento de texto horizontalmente
  - `text-align`
  - Especifica como o texto deve ser alinhado horizontalmente na caixa
  - `start / end`: o texto deve ser alinhado ao início/fim da linha do modo de escrita atual
  - `justify`: o texto deve ser alinhado às bordas direita e esquerda da caixa e para isso o navegador irá alterar o espaçamento entre palavras
- Orientação dos caracteres do texto
  - `text-orientation`
  - Altera a orientação dos caracteres do texto
  - `mixed`
  - `upright`
- Direção do texto
  - `direction`
  - `ltr`
  - `rtl`
  - Recomendado utilizar o atributo `dir` do HTML

## Fontes variantes

- São fontes que possuem muitas variantes de um mesmo tipo de letra num único arquivo, em contraste as fontes "normais" que requerem importar diferentes arquivos para diferentes versões do mesmo tipo de letra