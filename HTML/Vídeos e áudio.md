# Vídeos e áudio

- `<video>`:
  - `?src`: Caminho para o vídeo.
  - `?poster`: Caminho para o poster.
  - `?preload`: Buffering do arquivo
    - `none`
    - `metadata`: buffering de apenas metadados.
    - `auto`: deve fazer buffering do vídeo
  - `?(width / height)`:
    - por padrão o vídeo está na sua proporção nativa
    - caso não haja aspect ratio no tamanho definido, o vídeo irá crescer horizontalmente para preservar a proporção, com o espaço não preenchido tendo um fundo de cor sólida por padrão
  - `?muted`
  - `?loop`
  - `?autoplay`
- Como alternativa ao atributo `src`, podemos utilizar o elemento `source`, de tal forma que o navegador irá pegar o primeiro que achar.
  - `src`
  - `type`: tipo mime do arquivo. é recomendado colocar para que o navegador passe por essa fonte rapidamente caso não suporte
- `audio`
  - `?controls`
  - `?src`
  - podemos utilizar o `source` da mesma forma
- Dentro de ambos, podemos colocar um conteúdo **fallback**, que será mostrado se o navegador não suportar

## Arquivos de mídia

- Formatos de container (mp4, webm, etc.):
  - Definem uma estrutura para as faixas de áudio/vídeo, metadados, codecs etc.
  - Cada faixa de áudio/vídeo num container segue um formato de um codec, que é utilizado para codificar a mídia
  - Também podemos ter faixas sem nenhum ou o mínimo de container
- Codec:
  - Utilizado para compactar vídeo/áudio em dados binários e vice-verse
- Captions:
  - São transcrições de **tudo** do áudio, até sons não falados
  - Closed captions: Pode ser ativado/desativado
  - Open captions: Está embutido no vídeo
- Subtitles:
  - Incluem apenas traduções das falas

## Faixas de textos

- WebVTT é um formato de texto que
  - permite colocar uma string de texto (cue) em certo tempo do vídeo
  - e além de um pouco de estilo
- Elemento `track`
  - permite adicionar uma faixa de texto
  - o formato geralmente é webvtt, um formato de texto
  - `src`
  - `srclang`: linguagem da legenda
  - `kind`: tipo da cue
    - `subtitles`:
      - faixa para tradução apenas da fala
      - **tradução**
    - `captions`:
      - faixa para **transcrição** de sons importantes, até de sons que não são da fala. usados para pessoas que não conseguem ouvir
      - **problemas na audição**
    - `descriptions`:
      - descreve detalhes visuais importantes para pessoas com problemas de visão
      - **problemas na visão**

## Exercícios

1. Represente um vídeo com poster, com o buffering de vídeo ativado, com autoplay, mutado e com faixas de texto dos tipos `captions`, `subtitles` e `descriptions` e no mínimo 2 fontes.
2. O que é um formato de container e um codec?
3. Qual a diferença entre captions e subtitles? E open captions e closed captions?
4. Há faixas de vídeos sem containers?
5. O que acontece se o tamanho especificado para um vídeo não ser proporcional à sua relação largura-altura?