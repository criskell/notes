# Roteamento

- `@app.route()`: Vincula uma URL a uma função.
- Argumento `methods`:
  - Uma rota por padrão só responde métodos `GET`.
  - É uma lista de métodos da rota.
- Seções variáveis na URL:
  - Com os caracteres `<` e `>`, marcamos seções variáveis na URL.
  - As variáveis são passadas como argumentos palavra-chave.
  - Conversores:
    - Especificam o tipo do argumento.
    - `string`: Qualquer texto sem barra.
    - `int`
    - `float`
    - `path`: `==string`, mas aceita barras
    - `uuid`
  - `/<exemplo>`
  - `/<conversor:exemplo>`

## Trailing slash

- Se a rota tiver uma barra no final `/a/`, podemos acessar a URL com `/a` e deste modo o usuário será redirecionado para `/a/`. É similar a uma pasta num sistema de arquivos.
- Se a rota não tiver uma barra no final `/a`, não podemos acessar a URL com `/a/`. É similar ao caminho de um arquivo.

## Construção de URL

- `flask.url_for(fn, **kwargs)`:
  - Constrói um caminho absoluto para a função `fn`, passando todos os `kwargs` para cada parte variável da rota.

## Arquivos estáticos

- Crie uma pasta `static` no pacote ou ao lado do módulo.
- Gerar URLs:
  - Utilize o endpoint `static` com o argumento `filename`.