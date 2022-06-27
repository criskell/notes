# Dimensionamento

- Dimensionamento intrísico: Dimensionamento que ocorre pelo conteúdo ou naturalmente.
- Dimensionamento extrínsico: Dimensionamento explícito pelo autor.
- Dimensionando com porcentagens: A porcentagem é resolvida com base no bloco que contém o outro bloco.
- Margens e preenchimento com porcentagens: A porcentagem é resolvida com base no tamanho em linha do bloco que o contém. Em idiomas horizontais, seria a largura.
- Altura mínima & máxima (irá ter pelo menos essa largura ou no máx.): `min-height`, `max-height`
- Largura mínima & máxima (irá ter pelo menos essa altura ou no máx.): `min-width`, `max-width`. Caso de uso:
  - `img { max-width: 100%; }`: A largura intrísica da imagem não ultrapassará a largura do bloco pai.
- Unidades da viewport:
  - Viewport: Área visível no navegador.
  - vw: 1 unidade = a 1% da largura da viewport.
  - vh: 1 unidade = a 1% da altura da viewport.