# Tipos de caixas

- Tipo bloco:
  - Cria uma nova linha.
  - Ocupa todo a largura do elemento pai.
  - `width` e `height` aplicados.
  - margens, bordas e preenchimentos são aplicados e faz outros elementos se moverem.
  - os blocos fluem na direção de bloco.
  - a altura terá o tamanho necessário para caber o conteúdo.
  - margens podem ser colapsadas.
- Tipo em linha:
  - Não cria uma nova linha.
  - Ocupa o espaço necessário.
  - fluem na direção inline.
  - `width` e `height` não aplicados.
  - margens, bordas e preenchimentos horizontais são aplicados e faz outros elementos se moverem.
  - margens, bordas e preenchimentos verticais são aplicados e não faz outros elementos se moverem.
- Tipo `inline-block`:
  - São dispostas em linha numa caixa de linha e permite alterar largura/altura do elemento e margens e preenchimentos verticais.
  - `block` + `inline` == `inline-block`.