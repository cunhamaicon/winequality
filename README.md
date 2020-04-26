# winequality

Análise da qualidade dos vinhos

## Introdução

Nesse trabalho apresento um modelo de regressão utilizando XGBoost para determinar a qualidade dos vinhos baseado em suas  características. O modelo teve um erro quadrático médio de 0.61 e foi 29% melhor que o baseline.

Linguagem: Python

Autor: Maicon Henrique Cunha

## Arquivos:

1. winequality.csv - Base utilizada
2. winequality.ipynb - Arquivo principal onde são feitas todas as análises e gerado um modelo para prever a qualidade dos vinhos
3. winequality.html - Réplica do arquivo  winequality.ipynb porém no formato html
4. resultado.csv - Amostra de 20% da base com os dados originais e os dados previstos pelo modelo.
5. model.bin - Modelo salvo para utilização futura
6. apply_model.ipynb - Exemplo de aplicação do modelo em uma linha de forma manual

## Respostas:

a. A estratégia de modelagem seguiu o seguinte roteiro:

  1. Definição da abordagem do problema: regressão ao invés de classificação 
  2. Definição da função de erro
  3. Exploração da base para observação de inconsistências
  4. Remoção de amostras defeituosas
  5. Remoção de outliers
  6. Análise exploratória dos dados. Descoberta de variáveis importantes para o problema
  7. Preparação dos dados para utilização dos modelos
  8. Aplicação de diversos modelos de ML com validação cruzada
  9. Escolha de um algoritmo de ML e implementação de grid search para otimização dos parâmetros
  10. Validação do modelo de ML escolhido com atenção ao baseline
  11. Geração de arquivo(resultado.csv) com o resultado da aplicação do modelo em uma base de teste para comparação
  12. Modelo(model.bin) salvo para análises futuras
  13. Criação de arquivo (apply_model.ipynb) de teste pontual para o modelo

b. Como o problema foi abordado através de regressão a função de custo utilizada foi a raiz do erro quadrático médio. Essa função é de fácil interpretabilidade e se mostrou útil na solução do problema.

c. O modelo final escolhido apresentou o menor erro. ALém disso, possibilita facilmente observar as variáveis mais importantes e obter insights sobre a qualidade do vinho através da árvore de decisão.

d. Para a validação do modelo foi utilizada a validação cruzada. A validação cruzada evita que um conjunto mais favorecido ou menos favorecido escolhido aleatoriamente tenha impacto direto na avaliação do modelo. A atenção ao baseline é importante para garantir que o modelo possui inteligência.

e. Uma das evidências que o modelo é bom é o fato das variáveis mais importantes no modelo serem condizentes com a análise exploratória realizada anteriormente. Afirmo que ele é suficientemente bom pois foram realizados testes com diversos outros modelos de Machine Learning e o XGBoost com os parâmetros escolhidos através de grid search teve a melhor performance. Além disso o XGBoost é muito utilizado na comunidade de Machine Learning e tem histórico excelente de resultados.
