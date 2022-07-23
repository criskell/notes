# Estruturação do site

## Seções básicas de um site

- Cabeçalho:
  - Uma grande faixa preta no topo do site, que normalmente contém slogans, logotipos, etc.
  - Informações comuns para toda as páginas.

- Barra de navegação:
  - Fornece links para seções do site. Normalmente é definido dentro do header.

- Conteúdo principal:
  - Área central que armazena boa parte do conteúdo **exclusivo** da própria página.

- Barra lateral:
  - Contém informações periféricas, como anúncios, widgets, calendário, biografia do autor do post e etc.

- Rodapé:
  - Faixa que fica na parte inferior da página, normalmente com letras pequenas, para definir copyright, informações de contato e etc. São informações comuns para toda a página, mas que não são tão críticas.


## Representação da estrutura via HTML

- Devemos marcar seções de conteúdo com base em sua *funcionalidade* e assim, por exemplo, leitores de tela podem responder coisas como "encontre o conteúdo principal". Semântica: usar o elemento certo para o trabalho certo. 
- O HTML fornece tags semânticas que podemos utilizar para representar as seções básicas de um documento:
  - `main`:
    - Conteúdo **exclusivo** da página.
    - Somente 1 por página.
    - Recomendado que seja aninhado diretamente ao `body`
  - `article`:
    - Bloco de conteúdo que faz sentido por si só, sem o resto da página.
    - Autocontido
    - Pretende ser distribuído independentemente
    - Exemplos:
      - Posts de blog
  - `section`:
    - Agrupa uma única parte da página que constitui uma única peça de funcionalidade ou tema
    - É recomendado iniciar uma seção com um título, mas nem todas as seções precisam ter títulos
    - É um elemento genérico para seções autônomas que não possuem um elemento semântico mais específico para representar
    - Pode ser aninhado dentro de `article` ou inverso
    - Exemplos:
      - Grupos de artigos
  - `aside`:
    - Fornece informações adicionais indiretamente relacionado ao conteúdo principal.
    - Exemplos:
      - Biografia do autor
      - Links relacionados
  - `header`:
    - Conteúdo introdutório.
    - Se estiver definido no `body` vale para a página toda, se estiver no `article` vale pro `article` e etc.
  - `footer`:
    - Conteúdo de rodapé, geralmente no final da página.

### Wrapper não semânticos

- Utilizados para agrupar conteúdo e talvez manipular-los como uma única entidade
- Casos de uso:
  - Não queremos dar um significado extra
  - Não existe nenhum outro elemento semântico de bloco/inline ideal para agrupar
- `div`: Elemento não-semântico de nível de bloco
- `span`: Elemento semântico de nível inline

## Planejando um site

- Arquitetura de informação:
  - Planejar todo o conteúdo do site
  - Quais páginas, como elas se organizam e como se vinculam entre si
- Passos para planejar um site:
  1. Decidir o que vai ter de comum em cada página (header, footer, etc.)
  2. Criar a estrutura das páginas
  3. Listar os conteúdos exclusivos para cada página
  4. Agrupar estes conteúdos (ideias)
  5. Criar o mapa do site, com setas que mostra o fluxo de trabalho e com a página central no meio
