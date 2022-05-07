# HTML5

## Estrutura

- Utilizamos o HTML para aplicar formatações nas páginas.

```html
<!doctype html> <!-- define o tipo do documento -->
<html> <!-- elemento raiz para todos os elementos no DOM -->
    <head> <!-- seção HEAD -- Não aparece diretamente pro usuário -->
        <title>Título do site</title> <!-- Título do site -->        
    </head>
    <body> <!-- seção BODY - Aparece pro usuário -->
        Meu primeiro site
    </body>
</html>
```

## Cabeçalhos

- São títulos hierárquicos.
- H1 é o título principal e H2-H6 são subtítulos.

## Imagens

- Elemento `img`.

## Tabelas

- Tabelas são utilizadas para criar dados tabulares no HTML.
- Uma tabela é composta por cabeçalhos, colunas e linhas.
- Elementos:
  - `table`:
    - Representa uma tabela.
    - Atributos:
      - `align`: Alinha a tabela.
  - `tr`: Representa uma linha da tabela.
  - `td`: Representa uma célula.
    - `colspan="n"`: Permite alterar a extensão da célula para `n` colunas.
    - `rowspan="n"`: Permite alterar a extensão da célula para `n` linhas. Ou seja, ela irá ocupar mais linhas na tabela.
    - `height`: Altura da célula.
    - `align="a"`: Alinha o conteúdo da célula numa das seguintes posições:
      - `center`: Ao centro.
      - `left`: Esquerda.
      - `right`: Direita.
  - `th`: Representa um cabeçalho da tabela.

## Formulários

- Formulários são utilizados para capturar informações do usuário.
- Elementos:
  - `form`:
    - Representa um formulário.
    - Atributos:
      - `action`: Para onde os dados do formulário serão enviados.
  - `input`:
    - Representa uma entrada de dados.
    - Atributos:
      - `type`: Tipo da entrada.
      - `name`: Nome da entrada.