# Textos

- Um dos trabalhos do HTML é dar significado e estrutura de texto por meio de elementos

## Parágrafos e títulos

- A maioria dos textos estruturados possuem parágrafos e títulos.
- Parágrafos:
  - Criados com um elemento `p` envolvendo um conteúdo.
- Títulos:
  - Representados por `h(1-6)`
  - Cada elemento começa um conteúdo de nível diferente.
  - Possuem uma hierarquia: `h1` é o título principal, `h2` é o sub-título, `h3` é o sub-sub-título, etc.
  - Dicas para criar estruturas hierárquicas:
    - Um `h1` por página.
    - Ordem correta: `(h1) (h2) (h3) (h2) (h3)` (sim) `(h2) (h1) (h3)` (não)
    - Máximo três por página
- Por que utilizar marcação estrutural:
  - Os usuários buscam geralmente conteúdos na página por títulos (índice).
  - SEO: Palavras-chaves nos títulos
  - Acessibilidade
- Por que utilizar semântica:
  - **Significado** em oposição à **forma**.
  - Um elemento semântico permite saber o que significa, apenas olhando. Utilizamos semântica para saber a função de algo. **Se tiver a semântica errada, pode gerar problemas.**
  - `h1` é um elemento semântico, pois dá o significado ao conteúdo de "título de nível superior".
  - Por que é importante:
    - Acessibilidade e SEO

## Listas

- Não ordenadas:
  - A ordem dos itens **não importa**.
  - Envolvemos os itens (envolvidos pelo elemento `li`) em um elemento `ul`.
- Ordenadas:
  - A ordem dos itens **importa**.
  - = anterior, exceto que o container é `ol`.
- Aninhadas:
  - Quando colocamos uma lista dentro da outra.

## Ênfase e importância

- Ênfase:
  - Na linguagem humana, quando queremos dá ênfase, *enfatizamos*.
  - Na linguagem escrita, quando queremos enfatizar, escrevemos no estilo itálico.
  - Enfatizar altera sutilmente o significado da frase.
  - Elemento `em`.
  - Por que utilizar:
    - Acessibilidade (altera o tom da voz do leitor)
    - Torna o documento mais interessante em se ler
- Importância:
  - Na linguagem humana, para enfatizar palavras importantes, enfatizamos.
  - Na linguagem escrita usamos o negrito.
  - Elemento `strong` (palavras com forte importância)

## Elementos de apresentação

- São elementos sem semântica com valor representacional.
- Exemplos: `<i>`, `<u>`, `<strong>`.
- `<i>`: transmite um significado que é transmitido tradicionalmente via itálico, por exemplo: nomes científicos, termos técnicos, palavras estrangeiras.
- `<b>`: transmite um significado que é normalmente transmitido tradicionalmente via negrito, por exemplo: palavras-chaves, nomes de produtos.
- `<u>`: transmite um significado que é normalmente transmitido tradicionalmente via sublinhado, por exemplo: nome próprio e erros ortográficos.

## Exercícios

1. Em relação aos textos em páginas web, no que o HTML ajuda?
2. Por que dá significado (semântica) e estrutura aos conteúdos na web?
3. Descreva os títulos do HTML.
4. Diferencie os tipos de listas.
5. Como funciona a ênfase e importância no HTML? Por que enfatizar ajuda a página?
6. O que são elementos de apresentação? Dê exemplos e descreva cada um deles.