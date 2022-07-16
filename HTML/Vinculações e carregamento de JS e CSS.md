# Vinculações

## Elemento `link`

- Especifica um *relacionamento* com o documento atual e um **recurso externo**
- Casos de usos:
  - Vincular folhas de estilos
  - Estabelecer ícones
- Atributos:
  - `rel`:
    - O relacionamento entre o documento atual e o recurso externo.
    - Deve ser uma lista separada por espaços de *tipos de links*
  - `href`: URL do recurso vinculado
  - `type`:
    - Especifica o tipo MIME do recurso vinculado.
    - Para CSS, é recomendado que omitimos `type`.

### Favicons

- São pequenos ícones de um site.

## Tipos de links

- Indicam o relacionamento entre um documento e um recurso externo que está sendo vinculado pelo documento
- Alguns tipos são:
  - `canonical`: Define o recurso canônico (original) do conteúdo atual do documento
  - `next / prev / first / last`: Indica que o link leva para o próximo/anterior/primeiro/último recurso na sequência atual em que o documento está
  - `noreferrer`: Impede que ao navegar para outra página, o navegador envie um *referenciador* via HTTP
  - `nofollow`:
    - Indica que o documento vinculado não é endossado pelo autor.
    - Casos de uso:
      - Um link é um "mal exemplo"
      - Não há controle sobre o link
      - Há uma relação comercial entre os dois
  - `stylesheet`:
    - Indica uma folha de estilo do documento
    - Se `type` não definido, o navegador assume `text/css`

## Elemento `a`

- Cria um hiperlink para um recurso que uma URL pode endereçar
- Atributos:
  - `download`:
    - Indica que o recurso deve ser baixado.
    - O valor é opcional, se utilizado deve indicar uma sugestão de nome de arquivo
    - Só funciona para recursos na mesma origem
  - `href`:
    - URL que o hiperlink aponta.
  - `hreflang`: Linguagem do recurso apontado.
  - `referrerpolicy`: Controla o referenciador que deve ser enviado ao acessar o link.
  - `rel`:
    - Indica um relacionamento com a URL vinculada
    - Tipos de links separados por espaços
  - `target`:
    - Onde a URL deve ser aberta.
    - Um nome de um contexto de navegação.
    - Valores:
      - `_self`
      - `_blank`: geralmente uma nova guia
      - `_parent`: no contexto de navegação pai
      - `_top`: no contexto de navegação mais alto

## Exercícios

1. O que é o elemento `link` e como funciona o atributo `rel`? Como definir mais de um tipo de link em `rel`?
2. Devemos omitir o tipo MIME ao vincular uma folha de estilos externa ao documento?
3. O que são favicons?
4. Cite 5 *tipos de links* utilizados no atributo `rel` do elemento âncora e do elemento link.
5. Como funciona o `_target` do elemento âncora?
6. Como abrir um link no contexto de navegação de nível superior?
7. Um alvo sendo `_blank` faz com que o link sempre seja aberto numa nova guia? Ou tem uma escolha do usuário?
8. Qual o significado do atributo `referrerpolicy` no elemento âncora?
9. Qual o significado de `nofollow`?