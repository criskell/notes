# Elementos de seccionamento

- Elementos destinados a agrupar conteúdos.
- `header`:
  - Representa um conteúdo introdutório para um documento ou seção.
  - Exemplos do que pode conter:
    - um logotipo
    - nome do autor
    - links de navegação
- `section`:
  - Agrupa uma única parte da página que constitui uma única peça de funcionalidade ou tema
  - É um elemento genérico para seções autônomas que não possuem um elemento semântico mais específico para representar
  - Uso:
    - É recomendado iniciar uma seção com um título, mas nem todas as seções precisam ter títulos
    - Pode ser aninhado dentro de `article` ou inverso
    - Exemplos:
      - Grupos de artigos
- `article`:
  - Representa uma parte da página que pode ser distribuível e reutilizável.
  - Deve fazer sentido por si só, independentemente do resto do site.
  - Autocontido
- `aside`:
  - Representa um conteúdo que não é diretamente relacionado ao fluxo do texto do conteúdo circundante, mas ainda sim está ligado de alguma forma.
  - Um conteúdo adicional/de apoio.
  - Exemplos:
    - Barra lateral ao conteúdo principal.
- `nav`:
  - Fornecer links de navegação.
  - Não precisar fornecer apenas uma lista, pode fornecer links em parágrafos.
  - Nem sempre é necessário que todos os links devam estar neste elemento, geralmente somente os links principais de navegação. Por exemplo, não é necessário utilizar num elemento `footer`.
- `footer`:
  - Rodapé da página.
  - Casos de usos:
    - Informações de direitos autorais.

## Exercícios

1. Numa página há uma área que precisa ser agrupada como uma única parte do documento com uma funcionalidade única. Qual elemento semântico posso utilizar?
2. Nesta mesma área, há vários blocos de conteúdos que faz sentido por si só, sem o resto da página e que posso remover. Qual elemento semântico posso utilizar?
3. Nesta mesma página há uma área irmã desta área que constitui um único tema. Qual elemento semântico posso utilizar?
4. Qual elemento semântico seria apropriado para um comentário? Um comentário pode ser distribuído independentemente e pode fazer sentido por si só sem o resto do documento (autocontido).
5. Não consigo pensar em nenhum elemento para seccionar conteúdo. Qual elemento posso *pensar* em utilizar?

