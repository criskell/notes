# unittest

- O unittest provém um framework de testes junto com um test runner.

## Conceitos

- Fixture:
  - Preparação para um teste, junto com ações de limpeza.
  - Dados de entrada.

- Casos de teste:
  - É uma unidade individual de teste
  - Verifica uma resposta para um conjunto de entradas
- Suíte de testes:
  - Conjunto de casos de testes e/ou suíte de testes.
- Test runner:
  - Orquestra a execução dos testes e indica para o usuário.
- Parametrização:
  - Quando temos diversos testes que diferem apenas na entrada.

- Afirmação: Valida uma saída com um resultado esperado.

## Estrutura de um teste

- Antes devemos pensar sobre:
  - O que estamos testando
  - Qual deve ser a saída
- Passos
  1. Organizar as entradas
  2. Executar o código
  3. Afirmar

## Afirmações

- Métodos:
  - `.assertEqual(a, b) = a == b`
  - `.assertTrue(a) = bool(a) is True`
  - `.assertFalse(a) = bool(a) is False`
  - `.assertIs(a, b) = a is b`
  - `.assertIsNone(a) = a is None`
  - `.assertIn(a, b) = a in b`
  - `.assertRaises(a) -> <gerenciador de contexto>`



## Casos de teste

- Cada caso é uma classe que estende `unittest.TestCase`
- Cada teste no caso deve começar com `test`

## Executando o test runner

- Criando um entrypoint para a linha de comando:

  - ```python
    if __name__ == '__main__':
        unittest.main() # executa o testrunner, que descobre todos os testes neste arquivo que estendem TestCase
    ```

- Executando como módulo:

  - `python -m unittest <arquivo>`
  - `python -m unittest discover`: Executa todos os arquivos `test*.py` no diretório atual
  - `python -m unittest discover -s tests`: Especifica que deve executar os testes no diretório `tests`
  - `python -m unittest discover -t src`:  Especifica que o código-fonte fica em `src`, assim podemos importar corretamente.

## Efeitos colaterais

- Modificar um estado, chamada de API, etc.

### Lidando com efeitos colaterais

- SRP
- Mocking
- Utilizar testes de integração ao invés de testes de unidade

## Testes de integração

- Verifica se várias partes da aplicação funcionam juntas.
- Tem mais efeitos colaterais que os unitários.
- Separando dos testes unitários:
  - `tests/unit`, `tests/intergration`
  - `python -m unittest -s tests/intergration`
- Fixtures:
  - `tests/intergration/fixtures`