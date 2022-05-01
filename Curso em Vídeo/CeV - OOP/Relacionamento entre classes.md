# Relacionamento entre classes

## Agregação

- Agregação é conhecida como relacionamento "tem um".
- Na agregação, a parte do todo existe sem o todo, mas pode agregar informações ao todo.
- Multiplicidade:
  - Formatos:
    - *: Várias
    - 0..*: Nenhum ou várias
    - Não existe algo como 2..* ou somente 2


### Diagrama de classes

```
Na UML, uma agregação é representada por uma linha sólida com um losango na ponta.
Abaixo:
- Um lutador disputa uma luta e uma luta é disputada por lutadores;
- Um lutador disputa no mínimo (0) ou várias (*) lutas (multiplicidade=0..*).
- Uma luta é disputada por vários (*) lutadores. (multiplicidade=*)
- A letra `v` acima do "Luta" é o losango.
- A letra `>` depois do "disputa" indica o sentido da relação.

+----------------------------+ *   disputa >
|    Lutador                 |-------------------
+----------------------------+                  |
| - nome                     |                  |
| - nacionalidade            |                  |
| - idade                    |                  |
| - altura                   |                  |
| - peso                     |                  |
| - categoria                |                  |
| - vitorias                 |                  |
| - derrotas                 |                  |
| - empates                  |                  |
+----------------------------+                  |
| + apresentar()             |                  |
| + status()                 |                  |
| + ganharLuta()             |                  |
| + perderLuta()             |                  |
| + empatarLuta()            |                  |
+----------------------------+                  |
               				                    |
     								            v 0..*
                          +----------------------------+
                          | Luta                       |
						  +----------------------------+
						  | - desafiado                |
						  | - desafiante               |
                          | - rounds                   |
                          | - aprovada                 |
                          +----------------------------+
                          | + marcarLuta()             |
                          | + lutar()                  |
                          +----------------------------+
                          
                         
```

