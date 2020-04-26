# winequality

Análise da qualidade dos vinhos

Autor: Maicon Henrique Cunha

## Objetivo:

Criar um modelo para estimar a qualidade do vinho

## Arquivos:

1. winequality.csv - Base utilizada
2. winequality.ipynb - Arquivo principal onde são feitas todas as análises e gerado um modelo para prever a qualidade dos vinhos
3. winequality.html - Réplica do arquivo  winequality.ipynb porém no formato html
4. resultado.csv - Amostra de 20% da base com os dados originais e os dados previstos pelo modelo.
5. model.bin - Modelo salvo para utilização futura
6. apply_model.ipynb - Exemplo de aplicação do modelo em uma linha de forma manual

## Roteiro:

1. Definição da estratégia de abordagem do problema: regressão ao invés de classificação 
2. Exploração da base para observação de inconsistências
3. Remoção de amostras defeituosas
4. Remoção de outliers
5. Análise exploratória dos dados. Descoberta de variáveis importantes para o problema
6. Preparação dos dados para utilização dos modelos
7. Aplicação dos modelos de ML com validação cruzada
8. Escolhas de um algoritmo de ML e implementação de grid search para otimização dos parâmetros
9. Validação do modelo de ML escolhido com atenção ao baseline
10. Geração de arquivo(resultado.csv) com resultado da aplicação do modelo em uma base de teste para comparação
11. Modelo(model.bin) salvo para análises futuras
12. Criação de arquivo (apply_model.ipynb) de teste pontual para o modelo


