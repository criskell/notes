# Links para download

- O atributo **download** em um elemento âncora faz o documento referenciado pelo hyperlink ser baixado.

- O valor do atributo é **opcional**, mas quando **há** valor, deve ser o **nome do arquivo**.

- Não irá funcionar sem um servidor (ou seja, com o esquema de URI `file:`).

- Exemplos:

  ```html
  <a href="caminhoParaOArquivo.zip" download="novoNomeAqui.zip" type="application/zip">Baixar arquivo ZIP</a>
  ```

- Podemos usar o atributo **type** para especificar o mime type do arquivo.