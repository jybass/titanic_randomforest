# Previsão de Sobrevivência no Titanic com Random Forest

Este projeto utiliza um modelo de Machine Learning, especificamente um `RandomForestClassifier`, para prever a sobrevivência dos passageiros do Titanic. Ele foi desenvolvido como uma submissão para a competição do Kaggle.

**Link da Competição:** [Titanic: Machine Learning from Disaster](https://www.kaggle.com/c/titanic)

## Sobre o Projeto

O objetivo principal é treinar um modelo capaz de classificar se um passageiro sobreviveu ou não ao desastre do Titanic. O processo inclui a limpeza e preparação dos dados, a transformação de variáveis e o treinamento e avaliação do modelo.


* **Carregamento de Dados**: Utiliza a biblioteca `pandas` para carregar os datasets de treino e teste.
* **Limpeza de Dados**:
    * As colunas `Cabin` e `Age` foram removidas.
    * Linhas com dados ausentes na coluna `Embarked` foram removidas do conjunto de treino.
    * Valores ausentes na coluna `Fare` do conjunto de teste foram preenchidos com a mediana.
* **Engenharia de Features**:
    * A coluna `Sex` foi transformada em valores numéricos (0 para 'male', 1 para 'female').
    * A coluna `Embarked` foi transformada em valores numéricos (0 para 'S', 1 para 'C', 2 para 'Q').
* **Modelagem**:
    * Um modelo `RandomForestClassifier` com 90 estimadores é treinado.
    * As features utilizadas para o treino foram: `Pclass`, `Sex`, `SibSp`, `Parch`, `Fare`, `Embarked`.
* **Avaliação**: O desempenho do modelo é visualizado através de uma matriz de confusão gerada com `seaborn` e `matplotlib`.
* **Submissão**: Gera um arquivo de previsão para ser submetido no Kaggle.

## Tecnologias Utilizadas

* Python
* Pandas
* Numpy
* Scikit-learn
* Seaborn
* Matplotlib


## Observação

Este é o primeiro projeto submetido ao Kaggle, focando em um fluxo completo de trabalho de machine learning, desde a análise de dados até a geração do resultado final, os proximos passos são aumento da acurácia. Documentarei todas alterações aqui.
