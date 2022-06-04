# PIP

- PIP é um gerenciador de pacotes do Python. Permite instalar e atualizar pacotes que não fazem parte da biblioteca padrão do Python.
- Formas de usar o PIP:
  - Executando o PIP como um módulo:
    - `python3.10 -m pip`
    - Quando executamos o PIP via sistema (`pip`), pode ser que ele instale o pacote num `site-packages` de uma versão antiga do Python. Executar o PIP como um módulo evita isso. 
  - Virtualenv:
    - Os virtualenvs permitem isolar um projeto do sistema e de outros pacotes.
    - Vantagens:
      - Utilizar a versão correta do Python
      - Usar um pacote numa versão específica sem afetar outros projetos.
    - O Python tem um módulo embutido que permite criar virtualenvs: `venv`.
      - `python3.10 -m venv venv`: Cria um ambiente virtual de nome `.venv`.
      - Ativando um ambiente virtual: `source venv/bin/activate`
        - Aqui posso executar o Python executando apenas `python`.
      - Desativando um ambiente virtual: `source venv/bin/deactivate`
      - Ao ativar um ambiente virtual, podemos utilizar somente o comando `pip`.
- PyPI:
  - Site que hospeda pacotes do Python.
  - Ao instalar um pacote, o Python procura por padrão aqui.
- Instalando pacotes:
  - `install <pacote>`
  - Este comando irá instalar o pacote as dependências do próprio pacote.
  - Se não especificada, instala a versão mais recente.
  - Depois de instalar o pacote, só executar como qualquer pacote normal do sistema.
  - Usando um índice de pacotes customizados: `-i https://url.com`
  - Instalando a partir de um repositório do Git: `install git+https://github.com/meurepo`
  - Instalando um pacote no modo editável:
    - `install -e .`
    - Ao fazer isso, o PIP cria um link do diretório atual no diretório `site-packages` para o diretório atual.
  - Instalando `requirements.txt`: `install -r requirements.txt`
- Outros comandos:
  - `list`: Lista todos os pacotes instalados no ambiente.
  - `show`: Mostra informações específicas de um pacote no ambiente.
- Arquivo `requirements.txt`:
  - Serve para especificar os *requisitos* (pacotes/dependências externos) + suas versões.
  - Gerando os requisitos do ambiente atual: `freeze`
  - Com redirecionamento: `freeze > requirements.txt` 
  - No arquivo ao invés de utilizar operadores de igualdade, podemos utilizar outros operadores de comparação. Ao instalar o `requirements.txt`, o Python irá buscar a versão *mais recente* que *satisfaça* o requisito.
  - Atualizando agora: `install -U -r requirements.txt`
  - Podemos usar outra sintaxe: `pacote>=x.y.z, <a.b.c`: Ou seja, o Python irá buscar um pacote com a versão mais recente que seja maior ou igual a `x.y.z` e que seja menor que `a.b.c`.
  - Podemos ter `requirements_dev.txt` também. Adicionar `-r requirements.txt` no início do arquivo instala as deps. de produção.
- Desistalando pacotes:
  - `uninstall`

## Questões de revisão

1. O que é PIP?
2. Quais as vantagens de utilizar o PIP como um módulo?
3. O que são virtualenvs?
4. O que é o PyPI?
5. Como listar todos os pacotes no ambiente atual?
6. Como mostrar informações específicas de um pacote?
7. Para que serve a opção `-i` no comando `install`?
8. Como instalar um pacote a partir de um repositório Git?
9. O que é a instalação de um pacote no modo editável?
10. O que é o arquivo `requirements.txt` e como usar?
11. Para que serve a opção `-r requirements.txt` num arquivo `requirements.txt`?
12. O que isso faz num arquivo requirements.txt: `package>=1.0, <2.0`
13. Para que serve o comando `freeze` no PIP?
14. Como desistalar pacotes?
14. Como atualizar um pacote?