# Banco de dados

- Flask não é opinativo sobre o banco de dados.
- `flask-sqlalchemy`: Extensão wrapper do SQLAlchemy (ORM) para Flask.

## Tipos de banco de dados

- Relacional:
  - Segue o modelo relacional.
  - É melhor para dados estruturados.
- NoSQL:
  - Não segue o modelo relacional.
  - Indicado para dados que não seguem muito uma estrutura definida.

## SQLAlchemy

- É um ORM, ou seja, permite manipular banco de dados utilizando entidades de alto nível (classes, métodos e objetos).

## Configurando & inicializando

- Variáveis de configuração no Flask:
  - `SQLALCHEMY_DATABASE_URI`: Localização do banco de dados.
- Criar a instância do banco de dados, que representa o mesmo: `db = flask_sqlalchemy.SQLAlchemy`

## Modelos

- Classes que representam dados do banco de dados.

- ```python
  from app import db
  
  class User(db.Model):
      # ...
  ```

- Definimos os campos como variáveis de classe que armazenam objetos da classe `db.Column`.

- `db.Column(tipo-do-campo)`

## Relacionamentos

- Para relacionar tabelas, precisamos adicionar uma vinculação entre elas chamada de chave estrangeira em alguma tabela. Este campo guarda uma referência para um ID em outra tabela.

### Relacionamento um-para-muitos

- ```python
  class User(db.Model):
  	id = db.Column(db.Integer, primary_key=True)
      username = db.Column(db.String(64), index=True, unique=True)
      email = db.Column(db.String(128), unique=True, index=True)
      password_hash = db.Column(db.String(128))
      posts = db.relationship('Post', backref='author', lazy='dynamic')
  
  class Post(db.Model):
      id = db.Column(db.Integer, primary_key=True)
      body = db.Column(db.String(500))
      timestamp = db.Column(db.DateTime, index=True, default=datetime.utcnow)
      user_id = db.Column(db.Integer, db.ForeignKey('user.id'))
      
  post = Post(author=...) # não preciso lidar com a chave estrangeira, apenas com o campo de relacionamento.
  ```

- *Um* usuário possui *muitos* posts. *Muitos* posts possuem *um* usuário.

- `db.ForeignKey(key)`: Cria uma chave estrangeira para a tabela antes do ponto em `key` que referencia a coluna depois do ponto.

- `db.relationship(model, backref=backref, lazy=lazy)`:

  - É uma visão de alto nível de um relacionamento.
  - Num relacionamento *um-para-muitos*, definimos o relacionamento no lado "um" como um campo que armazena "muitos".
  - `model`: String que armazena o nome do modelo.
  - `backref`: Nome do campo que será adicionado no lado "muitos" (outro lado) para referencia o lado "um".
  - `lazy`: Define como deve ser feita a consulta deste relacionamento. 

### Objeto query

- Ponto de entrada para consultas no banco de dados.
- Métodos:
  - `.all()`: Retorna todas as linhas.
  - `.get(id)`: Obtém uma linha a partir do ID.
  - `.filter()`:
    - Retorna uma query que filtra o objetos.
  - `.first()`:
    - Conclui a query, retornando o primeiro objeto ou `None` caso não encontrar.



## Sessões

- Sessões guardam alterações feitas no banco de dados.
- `db.session`:
  - `.commit()`: Envia todas as alterações.
  - `.add(model)`
  - `.rollback()`: Aborta a sessão e remove as alterações da sessão atual.
