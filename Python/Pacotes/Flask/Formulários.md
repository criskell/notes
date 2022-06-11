# Flask-WTF

- Formulários podem receber dados do usuário.
- Liga a biblioteca `WTForms` com o `Flask`.

## Criando um formulário

- Representamos formulários através de classes que estendem `flask_wtf.FlaskForm`.
- Tipos de campos da `WTForms`:
  - `StringField`
  - `PasswordField`
  - `BooleanField`
  - `SubmitField`
- Validadores:
  - `DataRequired`
  - `EqualTo(field)`: O campo precisa ser igual ao campo `field`.
  - `Email()`:
    - Precisa ter o pacote `email-validator` instalado. 
- Para adicionar um campo, adiciona uma variável de classe utilizando algum tipo de campo, passando como primeiro argumento o rótulo do campo. Outros argumentos:
  - `validators`: Validadores de dados.

## Validando formulários

- Utilize o método `form.validate_on_submit`.
- Obtém os dados submetidos e valida.
- Retorna `False` se:
  - O método for `GET` ou
  - tiver um campo inválido.
- Retorna `True`, caso contrário.
- Podemos acessar os dados de um campo via `form.<campo>.data`

## Validação própria

- Todo método na classe no padrão `validate_<field-name>` será invocado além dos validadores do campo `field-name`, passando `field-name` como argumento.
- `ValidationError`: Exceção que podemos levantar passando como primeiro argumento a mensagem de erro.

## Exibindo formulários

- Passamos o formulário como variável no template.
- Métodos:
  - `form.hidden_tag()`: Exibe um campo com o token CSRF. Precisa ter a variável de configuração `SECRET_KEY`.
  - `form.<campo>.label`: Exibe o label do campo.
  - `form.<campo>(**kwargs)`: Exibe o HTML do campo, com os atributos passados como `kwargs`.
- Os validadores irão armazenar os erros de um campo como uma lista em`form.<campo>.errors`
