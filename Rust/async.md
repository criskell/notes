## core::future::Future

- É um trait da crate core
- Representa uma operação assincrona cujo resultado estará disponível em algum momento no futuro
- Em vez de bloquear a operação até que uma tarefa termine, uma Future permite que o programa continue executando outras tarefas enquanto a operação está pendente
- Quando o resultado estiver finalmente pronto, a Future produzira um valor do _tipo associado_ `Output`.
- Toda função declarada com async fn retorna na prática um tipo que implementa o trait Future.

## Polling

- O método poll é chamado por um _executor_.
- Esse método informa se ela já concluiu a execução (`Poll::Ready`) ou se ainda precisa aguardar um evento (`Poll::Pending`).
- Quando está pendente registra um _waker_ () para que o executor saiba quando deve chamá-la novamente, evitando busy waiting.

## Waker

- É um objeto usado pelo sistema assincrono do Rust para avisar o executor que uma Future pode continuar sua execução
- Quando uma Future ainda não pode ser concluida e retorna Poll::Pending, ela guarda (caso nao tenha terminado) ou utiliza o Waker (caso ela precisa ser executada novamente em breve ai ela chama o cx.waker().wake_by_ref() e retorna Poll::Pending, por exemplo, se detectar uma condição que fará progresso em uma proxima tentativa) recebido no Context para solicitar que o executor a execute novamente assim que o evento esperado ocorrer, como a chegada de dados de um socket ou o término de uma operação de I/O
- Assim o executor não precisa ficar verificando continuamente todas as futures para descobrir quais estão prontas

## `core::task::Context`

- É uma estrutura usada pelo sistema de Future do rust para fornecer informações e ferramentas necessárias durante a execução do método poll.
- O principal dado que ele carrega é um Waker.
