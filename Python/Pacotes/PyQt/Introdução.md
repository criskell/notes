# Introdução

## Conceitos introdutórios

- Widgets:

  - São componentes gráficos em forma retangular da GUI.
  - Passível de receber eventos do usuário ou de outra fonte. Ao receber um evento, emite um sinal para anunciar sua mudança de estado.
  - Widgets de nível superior não possuem pais.
  - Todos os widgets de nível superior são janelas.
  - Alguns widgets:
    - Botões
    - Rótulos: Utilizado para mostrar informações na forma de texto ou imagens.
- Gerenciador de layout:

  - Redimensiona e posiciona os widgets automaticamente, por exemplo, em eventos de redimensionamento.
- Loop de eventos:

  - Cada evento do usuário é adicionado na fila de eventos.
  - O loop de eventos é um loop infinito que aguarda um evento na fila.
  - Ao encontrar um evento, executa o manipulador dele.
  - Depois de executar, o loop agurda um novo evento novamente.
