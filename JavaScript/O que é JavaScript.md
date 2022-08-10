# O que é JavaScript

- JavaScript é uma linguagem de programação que permite adicionar comportamentos complexos e dinâmicos à uma página da web.
- Junto com HTML e CSS, forma uma pilha de camadas, onde:
  - HTML: Estrutura e significado
  - CSS: Estilo
  - JavaScript: Comportamento

## O que ele pode fazer

- Permite funcionalidades comuns de linguagens de programação, como:
  - variáveis
  - manipulação de textos e números
  - condicionais e loops
- Permite ouvir certos eventos numa página e reagir contra eles
- Manipulação de APIs:
  - Conjuntos de códigos prontos
  - Categorias:
    - APIs de navegador: Fornecido diretamente no navegador
      - DOM: API que permite manipular código HTML e CSS via JS.
    - APIs de terceiros: APIs não implementadas no navegador

## Como funciona o JavaScript

- Quando um navegador baixa uma página da web, o código desta página é executada num **ambiente de executação** (tab), juntos e **isoladamente** de outros ambientes para favorecer a segurança.
- Estes códigos são executados na ordem em que aparecem no código.
  - Se o JS for carregado **antes** de um elemento HTML, e depender deste elemento, irá ser gerado um erro.

- Quando o navegador interpreta um código, ele executa em ordem, de cima para baixo.

## Características

- Interpretada:
  - Códigos de linguagens interpretadas são executados diretamente a partir de seu código-fonte.
  - Browsers modernos implementam um JIT para executar o JavaScript, uma **compilação** em **tempo de execução**
  - Já em linguagens compiladas, a compilação é feita antes da execução.
- Lado do cliente (no caso de um navegador):
  - Código no lado do cliente é executado diretamente no seu navegador
  - Enquanto código no lado do servidor é executado no servidor e os resultados são mostrados para o usuário
- Dinâmica:
  - Significa que o JavaScript no lado do cliente pode gerar novos conteúdos no navegador e atualizar a página
  - Mas também esta palavra pode ser utilizada no lado do servidor, onde gera conteúdo diretamente no servidor
  - Estática quer dizer parada.

## Como adicionar JavaScript

- Interno:
  - Para adicionar JavaScript interno, adicionamos um elemento `script` no HTML, com o código JavaScript como sendo o conteúdo deste elemento
- Inline (via eventos):
  - É possível adicionar JavaScript diretamente em elementos HTML por meio de atributos para adicionar manipuladores de eventos, de forma inline.
- Externo:
  - Nesta forma, adicionamos JavaScript vinculando um arquivo externo utilizando o atributo `src`.

### Estratégias para carregar scripts

- Adicionar o script logo antes a tag de fechamento do elemento `body`.
  - O script será carregado logo após de todo o HTML ser analisado.
  - Bloqueia o carregamento e análise (parsing) do script até que todo o DOM do HTML seja carregado. Isto pode causar problemas de desempenho quando houver bastante scripts.
- elemento `script` sem atributos:
  - Ao longo do tempo de execução, o parsing do HTML está acontecendo.
  - Ao encontrar um script normal, todo este processo de parsing é bloqueado, e o script é baixado e executado, e após isso, o parsing volta ao normal.
- `async`:
  - Isto irá baixar o script ao mesmo tempo do carregamento da página.
  - Uma vez que o script é baixado, o processo de análise da página é pausada e o script é executado, depois da execução, o processo de parsing volta ao normal.
  - Não garante uma ordem de execução.
  - Quando usar:
    - Quando tiver vários scripts para rodar em segundo plano, e quer que eles estejam disponível o mais rápido possível, mas sem bloquear a página.
- `defer`:
  - Isto irá baixar o script ao mesmo tempo do carregamento da página.
  - Será executado após o processo de parsing da página completar.
  - A ordem entre scripts com `defer` é garantida.

## Comentários

- Comentários dão informações sobre o código para futuros leitores do código.
- Comentários podem serem de dois tipos:
  - Única linha
  - Múltiplas linhas

## Revisão

1. O que é JavaScript? O que eu posso fazer com JavaScript?
3. O que são APIs? Quais os tipos de APIs no JavaScript?
4. Qual é a diferença entre linguagem interpretada e compilada? Em qual categoria o JavaScript se encontra?
5. Qual é a diferença entre os termos dinâmico e estático relativo ao JavaScript?
6. Quais são as 3 formas de adicionar JavaScript à uma página?
7. Além de JavaScript, quais são as outras camadas que compõem uma pilha de código no lado do cliente?
8. Qual é a diferença entre código no lado do cliente e lado do servidor?
9. Quais são as 4 formas de carregamento de script (incluindo o elemento `script` antes da tag `</body>`).
10. Quais são as diferenças principais entre `defer` e `async`.
11. Quando usar um script com `async`?
12. `async` e `defer` podem funcionar em scripts *internos*?
13. Quais são os problemas com a estratégia de carregamento no final do elemento `body`?
