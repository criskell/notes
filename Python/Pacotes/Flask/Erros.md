# Erros

## Modo de depuração

- Mostra detalhes de erros no navegador
- Ativa o reloader, que ao ativar, irá reiniciar o server automaticamente ao modificar algum arquivo
- Permite manipular cada pilha do stack trace do erro, ver o código-fonte e executar código nesta pilha **remotamente**

## Páginas de erros personalizadas

- O decorador `app.errorhandler(code)` registra um manipulador de erro de código `code`
- Pode retornar uma tupla, onde o primeiro elemento é o conteúdo da resposta e o segundo é o código de status HTTP.

## Enviando erros via e-mail

- O pacote de logs que o Flask usa é `logging`
- Adicionamos handlers deste pacote via o método `app.logger.addHandler`

## Enviando erros para arquivos

- Classe `logging.RotatingFileHandler`
- Esta gira os logs, permitindo que não fiquem muito grandes.

## Categorias de logs

1. Debug
2. Info
3. Warning
4. Error
5. Critical