# Previsão do Preço de Casas

[Voltar](./)

## Sobre o Projeto

Este projeto consiste na aplicação de técnicas de Machine Learning para a tarefa de **Regressão**, com o objetivo de prever os preços de imóveis residenciais.

O estudo utiliza um conjunto de dados sintético criado para simular um mercado imobiliário real, contendo 10.000 observações e 13 características diversas, incluindo variáveis numéricas, ordinais e categóricas.

O objetivo principal é praticar a limpeza de dados, engenharia de características (Feature Engineering) e modelagem de regressão avançada para determinar o valor (`price_k_usd`) das casas.

Para ver o repositório completo [clique aqui](https://github.com/leonamcassemir0/previsao_preco_casa)

## Etapas do Projeto

O desenvolvimento do projeto seguiu as seguintes etapas principais:

1.  **Análise Exploratória de Dados (EDA):** Entendimento da distribuição das variáveis, identificação de *outliers* e análise das correlações com a variável-alvo.
2.  **Pré-processamento e Engenharia de Características:** Tratamento de valores ausentes, codificação de variáveis categóricas e criação de novas variáveis relevantes para o modelo.
3.  **Modelagem e Treinamento:** Aplicação e comparação de diferentes algoritmos de regressão (como Regressão Linear, Random Forests e Gradient Boosting).
4.  **Avaliação:** Análise das métricas de desempenho para selecionar o modelo mais robusto e preditivo.

## Visualização dos Dados (EDA)

![preco](https://github.com/leonamcassemir0/portfolio/blob/main/previsao_preco_casa/variaveis-categoricas.png)
![categoricas](https://github.com/leonamcassemir0/portfolio/blob/main/previsao_preco_casa/categoricas.png")

Oberva-se que as colunas estão bem distribuídas e com poucos outliers, o que indica que nosso modelo não precisará passar por modificações, podendo partir diretamente para o modelo!

## Modelo

Antes de partirmos para os resultados e avaliações, decidi colocaer uma breve contextualização do modelo.

Nas colunas `('building_material')` e `('heating_type')` temos mais de uma opção além de ser categótica. Isso para o modelo é ruim, mesmo fazendo um tratamento nas colunas, não podemos tratá-las diretamente com `OneHotEncoder()`, pois não temos apenas duas opções, mas podemos criar na mão colunas dummies(0 ou 1) para cada dado, como foi feito. Assim, nosso modelo ganha colunas a mais, porém melhora o treinamento do mesmo.
O restante das colunas foram tratadas normalmente com funções nativas da *SciKit-Learn*. **Agora vamos pros resultados obtidos!**

## Resultados e Desempenho

Após o treinamento, o modelo selecionado demonstrou a capacidade de criar previsões fortes e preditivas.

Obtemos as seguintes métricas de avaliação: 
- **Erro absoluto médio:** 47.96
- **Erro quadrático médio:** 3934.44
- **Raiz do erro quadrático médio:** 62.72
- **Porcentagem da média do erro absoluto:** 0.048
- **R-Quadrado:** 0.89

<img src="https://github.com/leonamcassemir0/portfolio/blob/main/previsao_preco_casa/real-previsto.png">

## Tecnologias Utilizadas

* **Linguagem:** Python
* **Ambiente:** Jupyter Notebook
* **Bibliotecas Principais:**
    * `pandas` (Manipulação e Análise de Dados)
    * `numpy` (Computação Numérica)
    * `scikit-learn` (Modelagem de Machine Learning)
    * `matplotlib` / `seaborn` (Visualização de Dados)

## Autor

Este projeto foi desenvolvido por Leonam Cassemiro, estudante de ciência de dados e engenharia de software. Críticas construtivas são sempre bem-vindas para aprimoramento contínuo.

* [LinkedIn](www.linkedin.com/in/leonam-cassemiro)
* [GitHub](https://github.com/leonamcassemir0)
* [Instagram](https://www.instagram.com/leonam.ds)
