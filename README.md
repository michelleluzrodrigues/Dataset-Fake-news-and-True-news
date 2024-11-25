# Dataset Fake News and True News Brazil

## Descrição

Este dataset reúne notícias de jornais brasileiros provenientes de diversas fontes, classificadas em duas categorias: notícias verdadeiras e notícias falsas. Ele foi desenvolvido com o objetivo de facilitar estudos e experimentos no campo de machine learning voltados para a detecção de fake news.

O texto das notícias passa por um cuidadoso pré-processamento, que remove elementos irrelevantes como pontuações, stopwords, URLs, números e palavras soltas que não contribuem para o contexto. Além disso, são aplicadas técnicas como lematização e normalização para transformar os textos em dados mais consistentes e adequados para treinar modelos de aprendizado de máquina de maneira eficiente.

O projeto contém duas pastas principais:
1. **unprocessed**: Contém os arquivos originais (`fake.csv` e `true.csv`), com as notícias conforme coletadas.
2. **preprocessed**: Será usada para armazenar os arquivos pré-processados, onde os textos terão sido lematizados e normalizados.

## Pré-processamento dos Dados

O pré-processamento foi projetado para otimizar a qualidade dos dados e melhorar a precisão da classificação. As etapas incluem:

1. **Remoção de Stopwords, Palavras Soltas e Pontuação**: Stopwords em português foram removidas, assim como palavras soltas que não contribuem para o contexto e pontuações irrelevantes.
2. **Lematização**: Reduzimos as palavras às suas formas básicas (lemmas).
3. **Remoção de URLs, Menções e Dígitos**: URLs, menções e números foram excluídos.
4. **Normalização de Texto**: Todo o texto foi convertido para letras minúsculas para evitar distinções entre maiúsculas e minúsculas.

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

## Licença

Este dataset está licenciado sob a [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). Isso significa que você pode:

- **Compartilhar**: Copiar e redistribuir o material em qualquer formato ou meio.
- **Adaptar**: Remixar, transformar e criar a partir do material para qualquer finalidade, mesmo comercialmente.

Desde que seja dada a devida atribuição à criadora:

**Atribuição**: Michelle Da Luz Rodrigues

![Creative Commons License](https://i.creativecommons.org/l/by/4.0/88x31.png)
