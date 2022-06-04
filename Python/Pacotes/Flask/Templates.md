# Templates

- São arquivos de texto que pode produzir qualquer formato baseado em texto.
- Vantagens:
  - Os templates separam a lógica do aplicativo da apresentação.
  - Não ter muito HTML no código Python.
  - Manter um layout padrão para todas as páginas.
- API:
  - `flask.render_template(template_name, **kwargs)`:
    - Renderiza o template `template_name` e passa `kwargs` como variáveis de template.
    - O template deve estar dentro do pacote ou na mesma pasta se for um módulo.