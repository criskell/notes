# Introdução

## O que é

- Flask é um microframework (framework minimalista) para criação de sites, APIs, microserviços e etc.
- Ser microframework quer dizer que o núcleo é simples, porém extensível.
- Ferramentas:
  - Werkzeug: Biblioteca para apps WSGI (interface entre Python e servidores web), implementa este padrão.
  - Jinja2: Motor de templates.

## Começando

- Importe a classe `Flask`: É a aplicação WSGI.
- Crie uma instância da classe: O primeiro argumento é o nome do pacote ou do módulo que o Flask utiliza para encontrar templates e arquivos estáticos.
- Utilize o decorador `route`: Ativa uma função ao entrar numa rota. O conteúdo padrão é o HTML.
- Rode a aplicação:
  - `export FLASK_APP=<modulo>`
  - `export FLASK_ENV=development`: Ativa todas as funcionalidades de desenvolvimento.
  - `flask run`:
    - Inicia o servidor de desenvolvimento
    - Ativa o modo de debug (que recarrega o código em alterações)