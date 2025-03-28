# Anonimizador de Nomes com BERT

Este projeto é um **anonimizador de nomes** utilizando o modelo BERT (Bidirectional Encoder Representations from Transformers) pré-treinado, com foco em **Reconhecimento de Entidades Nomeadas (NER)**. O código foi desenvolvido para anonimizar nomes de pessoas em textos e arquivos (Excel ou CSV).

## Funcionalidade

O objetivo do projeto é identificar e anonimizar automaticamente os nomes de pessoas em textos fornecidos, utilizando um modelo BERT pré-treinado, especificamente o modelo `lfcc/bert-portuguese-ner`. O modelo é utilizado para realizar a tarefa de **NER**, que tem como objetivo identificar entidades específicas dentro de um texto, como nomes de pessoas, organizações, locais, entre outros.

Neste código, o foco está em anonimizar **nomes de pessoas** nos textos, substituindo-os por asteriscos (`*`). A aplicação pode ser usada tanto para anonimização de texto livre quanto para anonimização em colunas de arquivos Excel ou CSV.

## Dependências

- **transformers**: Para carregar o modelo BERT e o tokenizer.
- **torch**: Para trabalhar com as operações do modelo.
- **pandas**: Para manipulação de dados em formato CSV e Excel.
- **os**: Para manipulação de caminhos de arquivos.

Instale as dependências necessárias utilizando o seguinte comando:

```bash
pip install transformers torch pandas
```

 --- 

 
## Como Usar

### Anonimizar Texto

Para anonimizar um texto:

```python
texto = "João foi ao supermercado e encontrou Maria."
texto_anonimizado = anonimizar_nome(texto)
print(texto_anonimizado)
# Saída: "**** foi ao supermercado e encontrou *****."
```

### Anonimizar Arquivo

Para anonimizar colunas de um arquivo CSV ou Excel:

```python
anonimizar_arquivo('arquivo.xlsx', 'arquivo_anonimizado.xlsx', 'TEXTO_LIVRE')
```

Este código anonimiza a coluna `TEXTO_LIVRE` e salva o resultado como `arquivo_anonimizado.xlsx`.
