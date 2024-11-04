# Fake News Detection in Portuguese

## Descrição do Projeto

Este projeto visa a detecção de notícias falsas e verdadeiras em português, utilizando um conjunto de dados coletado de fontes diversas. Realizamos o pré-processamento do texto para remover elementos irrelevantes e preparar os dados para o treinamento de modelos de machine learning.

O projeto contém duas pastas principais:
1. **unprocessed**: Contém os arquivos originais (`fake.csv` e `true.csv`), com as notícias conforme coletadas.
2. **preprocessed**: Será usada para armazenar os arquivos pré-processados, onde os textos terão sido lematizados e normalizados.

## Pré-processamento dos Dados

O pré-processamento foi projetado para otimizar a qualidade dos dados e melhorar a precisão da classificação. As etapas incluem:

1. **Remoção de Stopwords e Pontuação**: Stopwords em português foram removidas.
2. **Lematização**: Reduzimos as palavras às suas formas básicas (lemmas).
3. **Remoção de URLs, Menções e Dígitos**: URLs, menções e números foram excluídos.
4. **Normalização de Texto**: Todo o texto foi convertido para minúsculas para evitar distinções entre maiúsculas e minúsculas.

## Estrutura do Código

O código está no notebook `processed_text.ipynb`, com as etapas de pré-processamento organizadas em células, facilitando a execução sequencial. As seções principais incluem:

- **Carregamento dos Dados**: Carrega os arquivos `fake.csv` e `true.csv` da pasta `unprocessed`.
- **Funções de Pré-processamento**: Inclui a lematização e a remoção de elementos irrelevantes.
- **Salvamento dos Dados**: Salva os arquivos pré-processados na pasta `preprocessed`, nas subpastas `fake` e `true`.

## Como Executar

Para executar o projeto, siga estas etapas:

1. **Instale as Dependências**:
   - Certifique-se de ter o spaCy instalado e o modelo de português carregado:
     ```bash
     pip install spacy
     python -m spacy download pt_core_news_sm
     ```

2. **Execute o Notebook**:
   - Abra `processed_text.ipynb` e execute cada célula para carregar, processar e salvar os dados.

3. **Verifique os Resultados**:
   - Os dados processados serão salvos na pasta `preprocessed`, com subpastas `fake` e `true` contendo os arquivos CSV processados.

---

