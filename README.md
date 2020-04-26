# winequality

Análise da qualidade dos vinhos

## Introdução

Nesse trabalho apresento um modelo de regressão utilizando XGBoost para determinar a qualidade dos vinhos baseado em suas  características. O modelo teve um erro quadrático médio de 0.58 e foi 31% melhor que o baseline. Para chegar nesse resultado foi feita uma preparação dos dados criteriosa eliminando incosnsistências e outliers, uma análise exploratória para descobrir variáveis importantes e testes com vários modelos e parâmetros. 

Linguagem: Python

Autor: Maicon Henrique Cunha

## Arquivos:

1. winequality.csv - Base utilizada
2. winequality.ipynb - Arquivo principal onde são feitas todas as análises e gerado um modelo para prever a qualidade dos vinhos
3. winequality.html - Réplica do arquivo  winequality.ipynb porém no formato html
4. resultado.csv - Amostra de 20% da base com os dados originais e os dados previstos pelo modelo.
5. modelo_teste.bin - Modelo salvo para utilização futura com separação de treinamento e teste
6. modelo.bin - Modelo final utilizando todos os dados
7. apply_model.ipynb - Exemplo de aplicação do modelo em uma linha de forma manual
8. arvore.png - imagem com a inicio da arvore obtida no modelo

## Respostas:

a. Estratégia de modelagem:


  1. Definição da abordagem do problema: regressão ao invés de classificação   
  
  Embora as avaliações não sejam valores contínuos nesse trabalho será utilizada a abordagem da regressão. O porque dessa       abordagem fica claro com o exemplo:
  
  Caso1 - suponha que em 10 amostras para testes 2 estejam erradas: No erro 1 a avaliação original era 5 e o modelo avaliou
  como 6   No erro 2 a nota original era 7 e o modelo avaliou como 8
  
  Caso2 - suponha que em 10 amostras para testes 2 estejam erradas: No erro 1 a avaliação original era 5 e o modelo avaliou  
  como 8   No erro 2 a nota original era 7 e o modelo avaliou como 4
  
  Claramente os dois erros são diferentes! Porém se estivéssemos utilizando classificação teríamos uma mesma acurácia de 80%.
  Com um modelo de regressão e utilizando raiz do erro quadrático médio por exemplo essas diferenças são levadas em 
  consideração, sendo esse o motivo de utilizar regressão e como função de custo a raiz do erro quadrático médio
  
  2. Definição da função de erro
  3. Exploração da base para observação de inconsistências
  4. Remoção de amostras defeituosas
  5. Remoção de outliers
  6. Análise exploratória dos dados. Descoberta de variáveis importantes para o problema
  7. Preparação dos dados para utilização dos modelos
  8. Testes com diversos modelos de ML com validação cruzada. Kfold = 20
  9. Escolha de um algoritmo de ML e implementação de grid search para otimização dos parâmetros
  10. Validação do modelo de ML escolhido com kfold = 20 e atenção ao baseline
  11. Geração de arquivo(resultado.csv) com o resultado da aplicação do modelo em uma base de teste para comparação
  12. Modelo(model.bin) salvo para análises futuras
  13. Criação de arquivo (apply_model.ipynb) com possibilidade de teste pontual para o modelo

b. Como o problema foi abordado através de regressão a função de custo utilizada foi a raiz do erro quadrático médio. Essa função é de fácil interpretabilidade e se mostrou útil na solução do problema.

c. O modelo final escolhido apresentou o menor erro. Além disso possibilita facilmente observar as variáveis mais importantes e obter insights sobre a qualidade do vinho através da árvore de decisão.

d. Para a validação do modelo foi utilizada a validação cruzada com Kfold = 20. A validação cruzada evita que um conjunto mais favorecido ou menos favorecido escolhido aleatoriamente tenha impacto direto na avaliação do modelo. Além disso lida com o problema de overfiting. A atenção ao baseline é importante para garantir que o modelo possui inteligência.

e. Uma das evidências que o modelo é bom é o fato das variáveis mais importantes no modelo serem condizentes com a análise exploratória realizada anteriormente. Afirmo que ele é suficientemente bom pois foram realizados testes com diversos outros modelos de Machine Learning e o XGBoost com os parâmetros escolhidos através de grid search teve a melhor performance. Além disso o XGBoost é muito utilizado na comunidade de Machine Learning e tem histórico excelente de resultados.
