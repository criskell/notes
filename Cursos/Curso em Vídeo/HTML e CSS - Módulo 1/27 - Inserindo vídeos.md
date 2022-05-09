# Inserindo vídeos

- Vídeos são inseridos com a tag `video`.
- O elemento pode conter zero ou mais elementos `source` e um conteúdo **fallback**.
- O elemento `source` é utilizado para especificar mais de uma fonte de vídeo. O navegador irá escolher de cima para baixo o elemento `source` mais adequado, por exemplo, uma fonte suportada pelo navegador.
- O conteúdo **fallback** é exibido caso o navegador não suporte o elemento `video`.
- Atributos:
  - `src`: URL do vídeo. É opcional; Podemos usar o elemento `source`.
  - `preload`: Indica o pré-carregamento do vídeo. Possui 3 valores:
    - `none`: Nada deverá ser baixado.
    - `metadata`: Apenas os metadados deve ser baixado.
    - `auto`: Pode baixar o vídeo, mesmo que ele nunca seja iniciado.
  - `poster`: URL do poster do vídeo. Opcional.
