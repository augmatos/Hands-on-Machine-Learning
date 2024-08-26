# Documentação do Projeto de Extração e Treinamento de Modelos de NLP

## 1° Passo: Extração de Texto dos PDFs

1. **Selecionar Certidões de Penhor:**
   - Escolha certidões de penhor positivas em PDF que podem ser copiadas e coladas para análise.

2. **Executar o Script de Extração:**
   - **Script:** `1 - extracao_pdf`
   - **Descrição:** Este script extrai e trata o texto dos PDFs selecionados e armazena os dados em um arquivo JSON chamado `all_documents.json`.
   - **Formato do Arquivo JSON:**
     ```json
     [
         {
             "index": 0,
             "filename": "8832.pdf",
             "text": "Texto do PDF",
             "CPF/CNPJ": "",
             "Safra": [""],
             "Produto": [""],
             "Credor": [""],
             "Número do Registro": [""],
             "Quantidade": [""],
             "Número de Matrícula": [""]
         }
     ]
     ```

## 2° Passo: Anotação Manual das Entidades

- **Descrição:** Nomeie manualmente as entidades contidas no texto extraído para prepará-las para o treinamento do modelo de NLP.

## 3° Passo: Preparação dos Dados para Treinamento

- **Executar o Script de Anotação:**
  - **Script:** `2 - anotacao_entidades.py`
  - **Descrição:** Este script lê o arquivo `all_documents.json` com as entidades nomeadas e prepara os dados para treinamento do modelo.

## 4° Passo: Criação do Arquivo de Configuração

- **Descrição:** Este passo é necessário apenas para criar o arquivo de configuração com os hiperparâmetros para o treinamento.
- **Executar o Comando:**
  ```bash
  python -m spacy init config config.cfg --lang pt --pipeline ner --optimize accuracy --transformers
