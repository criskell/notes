## Margem vs preenchimento

| Margem                                                       | Preenchimento                                                |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| Fora da caixa                                                | Dentro da caixa                                              |
| Espaçamento do elemento entre elementos irmãos               | Espaçamento do elemento entre elementos filhos               |
| Separa a borda da caixa, de dentro para fora                 | Separa a borda da caixa, de fora para dentro                 |
| Pode afetar o espaçamento no pai do elemento                 | Pode afetar as dimensões do elemento                         |
| Por ocorrer fora da caixa, propriedades como `background` afetam somente se for do elemento pai | Por ocorrer dentro da caixa, coisas como fundo da caixa e scrollbars, vão até o preenchimento |
| Se for negativa, reduz o espaçamento entre pai/irmãos        | Não é permitido preenchimento negativo                       |