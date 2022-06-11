# Migrações

- Utilizada para atualizar um banco de dados a medida que o aplicativo muda ou cresce.
- Extensão `flask-migrate`:
  - Wrapper para `Alembic` (framework de migrações para SQLAlchemy).

## Inicializando

- ```python
  migrate = Migrate(app, db)
  ```

## Repositórios

- Guardam scripts de migração (alterações do banco de dados).
- Para aplicar estes scripts, devemos aplicar-los em sequência.
- `flask db init`: Cria o repositório de migrações.

## Criando migrações

- Automaticamente:
  - `flask db migrate [-m <mensagem>]`
  - O framework compara o scheme atual com o scheme definido pelos modelos e gera um script para que o scheme atual se iguale ao scheme dos modelos.
- Manualmente:
  - Criando os arquivos do zero

## Script de migração

- Possui as funções:
  - `upgrade`:
    - Aplica a migração.
    - `flask db upgrade`:
      - Aplica todas as migrações.
      - O framework primeiro verifica se o banco de dados está atualizado a última *revisão* do esquema. Se não estiver, executa todas as migrações criadas após a versão anterior.
  - `downgrade`: Desfaz a migração.