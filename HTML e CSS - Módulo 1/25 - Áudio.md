# Áudio

- Áudio pode ser inserido com a tag `audio`.
- Atributos:
  - `autoplay`: Inicia automaticamente o áudio.
  - `controls`: Ativa os controles do áudio.
  - `preload`: Indica o pré-carregamento do áudio. Pode ter os seguintes valores:
    - `none`: Não deve carregar nada antes do usuário iniciar o áudio.
    - `metadata`: Deve baixar apenas os metadados do áudio como duração.
    - `auto`: Permite baixar o áudio completo mesmo que o usuário **nunca inicie** ele.
  - `src`: Indica a URL do áudio. É opcional caso haja elementos `source` dentro.
- Dentro da tag, podemos ter elementos `source` .
- Podemos ter um **conteúdo** dentro das tags também, para agir como um fallback caso o navegador **não suporte** áudio.
- O elemento `source` especifica mais de uma fonte de áudio. O navegador irá escolher a fonte **mais adequada**, de cima para baixo, por exemplo, caso suporte o formato do áudio.
  - Atributos:
    - `src`: URL da fonte.
    - `type`: Mime type da fonte (recomendado utilizar).
