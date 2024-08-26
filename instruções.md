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

## 5° Passo: Validação de Erros

- **Executar o Comando:**
  ```bash
  python -m spacy debug data ./config.cfg --verbose
- **Descrição:** Este comando ajuda a identificar e corrigir erros na configuração e nos dados de treinamento do modelo. Ele fornece um diagnóstico detalhado dos problemas encontrados, o que é útil para ajustar a configuração e melhorar a qualidade do modelo.

## 6° Passo: Treinamento do Modelo

- **Descrição:** Este passo inicia o treinamento do modelo de NLP usando a configuração definida no arquivo `config.cfg` e os dados preparados no arquivo `training_data.spacy`.
- **Executar o Comando:**
  ```bash
  python -m spacy train config.cfg --output ./model --paths.train ./training_data.spacy --paths.dev ./training_data.spacy
- **Descrição:** O comando treina o modelo e salva o modelo treinado no diretório `./model`, usando os dados de treinamento e validação especificados.

## 7° Passo: Validação e Teste do Modelo

- **Descrição:** Após o treinamento, o modelo é avaliado com dados de validação para verificar sua eficiência e desempenho. Isso é essencial para garantir que o modelo generalize bem para novos dados.

- **Executar o Script de Metrica:**
  - **Script:** `4_metricas.py`
  - **Descrição:** Este script carrega o modelo `./model/best-model`, lê o arquivo `test_data.spacy` e avalia o desempenho geral do modelo.
- **Executar o Script de Metrica:**
  - **Script:** `5_metricas_por_entidades.py`
  - **Descrição:** Este script carrega o modelo `./model/best-model`, lê o arquivo `test_data.spacy` e avalia o desempenho do modelo para cada uma das entidades.

## 8° Passo: Atualização e Melhoria Contínua do Modelo

- **Descrição:** Após a validação de erros, o modelo treinado é utilizado para realizar a extração de dados, o que permite aumentar a quantidade de dados de treinamento. Isso resulta em um ciclo contínuo de aprimoramento do modelo. Cada novo ciclo de treinamento utiliza o modelo atualizado para melhorar suas previsões e gerar novos modelos.
