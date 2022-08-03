# Modo de escrita

- O modo de escrita refere-se a **direção do fluxo de bloco** e a **direção de conteúdo de nível inline** (**verticalmente** ou **horizontalmente**).
- Propriedade `writing-mode`:
  - `vertical-rl`: O fluxo dos blocos é da direita para a esquerda. O texto flue verticalmente. (verticalmente da direita para esquerda).
  - `vertical-lr`: O fluxo dos blocos é da esquerda para a direita. O texto flue verticalmente. (verticalmente da esquerda para a direita).
  - `horizontal-tb`: O fluxo dos blocos é de cima para baixo. O texto flue horizontalmente (horizontalmente de cima para baixo).
- Dimensão de bloco é sempre a direção em que os blocos fluem e dimensão inline é a direção que os conteúdos nível inline fluem.
- `inline-size` é o tamanho na dimensão em linha e `block-size` é o tamanho na dimensão de bloco.
- Propriedades lógicas/relativas ao fluxo: Temos propriedades **físicas** (width, border-left) mapeadas de acordo com as direções do modo de escrita.
  - `block-size`: Tamanho na dimensão de bloco. Por exemplo, se tivermos numa escrita `vertical-rl`.
- Também temos valores, como `inline-end`.