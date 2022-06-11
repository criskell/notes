# Autenticação

## Hashing de senhas

- Senha -> longa string codificada através de operações de criptografia que não possui uma função inversa.
- API:
  - `werkzeug.security.generate_password_hash(password)`
    - Esta função não é determinística, gera várias hashes para uma mesma senha. Isso previne saber que dois usuários tem a mesma senha.
  - `werkzeug.security.check_password_hash(hash, currentPassword) -> bool`

## Flask-Login

- Uma extensão que salva o estado de login do usuário.
- Como implementar:
  - Adicionar: `login = flask_login.LoginManager(app)`
  - Estender o mix-in`UserMixin` no modelo de usuário:
    - Implementa métodos e propriedades genéricas, obrigatórios da extensão, para login, apropriados para a maioria das classes.

### Métodos & propriedades do modelo de usuários

```python
class User(...):
    @property
    def is_anonymous(self):
        """
        Retorna True se o usuário for anônimo, ou seja, não estiver autenticado.
        """
  		# ...
```



### Carregador de usuários

- ```python
  @login.user_loader
  def load_user(id):
      # ...
  ```

- A extensão mantém o registro do usuário na *sessão de usuário* (cada usuário possui um espaço que permite armazenar dados de sessão) armazenando o ID.

- Quando o usuário entra numa página, a extensão pega este ID e chama o user loader para carregar um usuário.

## Autenticando e obtendo o usuário

```python
from flask_login import current_user, login_user

# current_user: objeto que representa o cliente do request obtido a partir do banco de dados ou um objeto especial para um usuário anonônimo.
# login_user(user, remember_me: bool): Salva o estado de login do usuário. remember_me indica se o usuário irá permanecer autenticado ou não.
```

### Protegendo páginas contra usuários anônimos

- ```python
  from flask_login import login_required
  
  @app.route('/')
  @login_required # <-- adicione este decorator
  def index():
      # ...
  ```

- Este decorator redireciona para a rota de login se o usuário for anonônimo.

- O atributo `login.login_view` precisa armazenar o nome da view function de login.
