# Configurações

- Temos diversos formatos para armazenar configurações, hardcoded, num arquivo separado e etc.
- O atributo `config` do objeto `Flask` pode agir como um dicionário que armazena as configurações do aplicativo.

## Carregando configurações com classes

- Permite a separação de preocupações (separation of concerns), separando o aplicativo das configurações.

- Criamos uma classe:

  - ```python
    import os
    
    class Config:
        SECRET_KEY = os.environ.get('SECRET_KEY')
    ```

- Carregamos um objeto com configurações utilizando `config.from_object(objeto)`:

  - ```python
    config.from_object(Config)
    ```

    