# Textos

- Um dos trabalhos do HTML é dar significado e estrutura de texto por meio de elementos

## Parágrafos e títulos

- A maioria dos textos estruturados possuem parágrafos e títulos.
- Parágrafos:
  - Criados com um elemento `p` envolvendo um conteúdo.
  - A tag final pode ser omitida em alguns casos.
- Títulos:
  - Representados por `h(1-6)`
  - Cada elemento começa um conteúdo de nível diferente.
  - Possuem uma hierarquia: `h1` é o título principal, `h2` é o sub-título, `h3` é o sub-sub-título, etc.
  - Dicas para criar estruturas hierárquicas:
    - Um `h1` por página.
    - Utilizar os títulos corretos para representar certo nível de conteúdo. Por ex.: h2 para representar sub-títulos e h3 para representar subtítulo do h2 (correto) h2 para representar sub-sub-títulos e h3 para sub-títulos
    - Pular títulos: `<h1> <h3> <h6>` (código incorreto)
    - Máximo três níveis por página
- Por que utilizar marcação estrutural para textos:
  - Os usuários buscam geralmente conteúdos na página por títulos (índice).
  - SEO: Palavras-chaves nos títulos
  - Acessibilidade
- Semântica:
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
  - Atributos:
    - `start`: início da contagem. deve ser um número, ou um n. equivalente
    - `value`: valor **numérico** do `li`. deve ser um número, ou um n. equivalente
    - `reversed`: inicia a contagem de forma regressiva. Se tiver elementos em excesso, o contador irá pro zero, depois pro -1, -2, etc.
- Aninhadas:
  - Quando colocamos uma lista dentro da outra.

## Ênfase e importância

- Ênfase:
  - Na linguagem humana, quando queremos dá ênfase, *enfatizamos*.
  - Na linguagem escrita, quando queremos enfatizar, escrevemos no estilo itálico.
  - Enfatizar altera sutilmente o significado da frase.
  - Elemento `em`.
  - Por que utilizar:
    - Acessibilidade (altera o tom da voz do leitor de tela)
    - Torna o documento mais interessante em se ler
- Importância:
  - Na linguagem humana, para enfatizar palavras importantes, enfatizamos.
  - Na linguagem escrita usamos o negrito.
  - Elemento `strong` (palavras com forte importância)

## Elementos de apresentação

- São elementos sem semântica com valor representacional.
- Exemplos: `<i>`, `<u>`, `<b>`.
- `<i>`: transmite um significado que é transmitido tradicionalmente via itálico, por exemplo: nomes científicos, termos técnicos, palavras estrangeiras.
- `<b>`: transmite um significado que é normalmente transmitido tradicionalmente via negrito, por exemplo: palavras-chaves, nomes de produtos.
- `<u>`: transmite um significado que é normalmente transmitido tradicionalmente via sublinhado, por exemplo: nome próprio e erros ortográficos.

## Listas de descrição

- O elemento `dl` representa uma lista de descrição
- Envolve um grupos de termos (`dt` - description term) e definições (`dd` description definition/details)
- Cada termo pode ter 1 ou N descrições imediatamente adjacentes.

## Citações

- `blockquote`:
  - Citações em bloco são seções retiradas de conteúdo de nível de bloco (citações estendidas).

- `q`:
  - Citações em linha são citações curtas, no meio do texto.

- Atributo `cite` nos elementos `q` e `blockquote`:
  - Indica a fonte da citação por uma URL

- Elemento `cite`:
  - Título do trabalho citado, como o nome de um livro, jogo, etc.
  - Pode ser usado dentro de um `blockquote`


## Abreviações

- `abbr`: abreviação ou acrônimo, com o termo expandido dentro do atributo `title`.

## Informações para contato

- O elemento `address` envolve informações de contato (telefones, endereço residencial e etc.)
- Sobre o elemento `article` ou `body` mais próximo.
- Pode ser colocado por exemplo num `footer` de um `article`.

## Sobrescrito e Subscrito

- Utilizar somente para conveções tipográficas.
- Casos de uso: Marcar datas, fórmulas químicas, equações e etc. para que tenham o significado correto.
- `sup`: Sobrescrito
- `sub`: Subscrito

## Códigos

- `code`:
  - Marcar códigos genéricos
  - Pequenos trechos de códigos. Para mostrar várias linhas utilize dentro de um `<pre>`

- `pre`:
  - Texto pré-formatado
  - Marcar código que deve ter seus espaços em branco preservados, do mesmo jeito que está no código da página

- `kbd`: Para marcar entrada do teclado **inserida**.
- `samp`: Para marcar a saída de um programa (**samp**le).

## Data e hora

- O elemento `time` permite marcar data/hora num formato legível por máquina (acessado via o atributo `datetime`).

## Quebras de linhas e linhas horizontais

- `br`:
  - Quebra de linha
  - Utilizar quando a quebra de linha é significativa (como um poema e endereços)
- `hr`:
  - Denota uma quebra temática no texto e não apenas uma linha horizontal (semântico)
  - Exemplos:
    - Mudança de tópico

## Texto inserido, marcado e deletado

- `ins`: Representa intervalo de texto que foi inserido ao documento.
- `del`: Representa intervalo de texto que foi deletado do documento.
- `mark`:
  - Representa um texto marcado/destacado
  - Possui fins de referência/notação
  - Possui relevância
  - Difere do strong: grau de *relevância* e não de importância
- `s`: Coisas que não são relevantes nem mais precisas.

## Exercícios

1. Em relação aos textos em páginas web, no que o HTML ajuda?
2. Por que dá significado (semântica) e estrutura aos conteúdos na web?
3. Descreva os títulos do HTML.
4. Diferencie os tipos de listas.
5. Como funciona a ênfase e importância no HTML? Por que enfatizar ajuda a página?
6. O que são elementos de apresentação? Dê exemplos e descreva cada um deles.
7. Quais as formas de representar citações?
8. Por que e como utilizar o elemento `time`?
9. Quais são as formas de representar códigos de computador?
10. Como representar listas de descrições?
11. Como utilizar subscrito e sobrescrito?
12. Como utilizar abreviações?
13. Qual é a diferença entre strong e mark?
14. O que é o elemento mark?
15. Como representar textos não precisos ou não relevantes semanticamente?
16. Ao que o elemento `address` se refere?