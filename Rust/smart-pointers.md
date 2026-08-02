# alloc::sync::Arc

- É um smart pointer que permite multiplas partes do software compartilhar ownership
- Utiliza um contador de referencia atomico
- Ao passar por um clone o contador de referencia incrementa
- Quando é destruida o contador é decrementado
- Objeto é liberado automaticamente quando a ultima referencia deixa de existir
- Não torna o conteúdo mutável de forma segura por si só
- `std::sync::Arc` importa da crate alloc

## Quais os usos?

- Compartilhar o mesmo objeto entre várias partes do programa sem precisar copiar os dados
- Cria um Arc e clona ele usando `Arc::clone(&arc)` (uma operação barata)
- Cada clone passa a apontar para a mesma alocação na memória
