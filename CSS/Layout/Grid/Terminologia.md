# Terminologia

- Container:
  - Elemento que contém uma grid
  - Cria um novo contexto de formatação de grid para seus filhos (itens) diretos.
- Item:
  - Elemento que é filho direto de um container.
- Line:
  - São linhas horizontais e verticais dividem a grade
  - Podem ter um nome
  - São numeradas a partir do 1 e valores negativos contam a partir do final
  - Esta numeração segue o modo de escrita e a direção de escrita (LTR/RTL)
- Track:
  - Espaço entre duas lines adjacentes
  - Colunas ou linhas da grade
- Cell:
  - Intersecção entre uma linha e coluna
  - Menor espaço num container
  - Delimitada por 4 lines
  - Por padrão, cada item irá ficar numa célula.
- Area:
  - Espaço no grid com 1 ou N cells
  - Delimitada por 4 lines
  - Podem ser referido pelas suas linhas ou por um nome
- Gap:
  - Gutter (espaçamento) entre trilhas.
  - Agem como uma trilha normal (apenas para dimensionamento).