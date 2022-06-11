# Shell

- `flask shell`:

  - Executa o interpretador num contexto de shell.

  - Contexto de shell é uma "lista" de símbolos para importar automaticamente.

  - ```python
    @app.shell_context_processor
    def make_shell_context():
        return {'db': db, 'app': app}
    ```

