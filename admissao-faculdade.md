[voltar](./)

# Previsão de admissão em faculdade

![Faculdade](https://raw.githubusercontent.com/leonamcassemir0/portfolio/main/facul.jpeg)

## Introdução

Baseado no dataset [admission](https://www.kaggle.com/datasets/safaruzzamanshovo/graduate-admission-dataset) do kaggle, irei criar um modelo utilizando árvore de decisão que prevê se o aluno, mediante suas notas e recomendações, passará para alguma universidade.

## Informações

### Colunas
![Colunas](https://raw.githubusercontent.com/leonamcassemir0/portfolio/main/colunas_dataframe.jpg)

#### GRE Score (Até 340)
É uma medida da preparação do candidato para o trabalho de nível de pós-graduação.Uma boa pontuação no GRE é geralmente considerada 158 para Verbal, 159 para Quantitativo e 4,5 para Redação, com uma pontuação geral de 318.

#### TOEFL Score (Até 120)
Avalia sua proficiência em inglês por meio de um teste que avalia quatro habilidades principais(leitura, compreensão auditiva, expressão oral e expressão escrita). 
Cada seção é pontuada em uma escala de 0 a 30, com uma pontuação total possível de 120. 
As pontuações são usadas por universidades e instituições em todo o mundo para avaliar sua preparação para a comunicação acadêmica e profissional em inglês.
Uma pontuação de 100 ou mais é geralmente considerada boa, enquanto pontuações acima de 25 em qualquer seção indicam proficiência avançada.

#### University Rating (Até 5)
Pontuação das faculdades pretendidas pelos alunos. Elas foram avaliadas em uma escala de 1 a 5, com 1 sendo ruim e 5 uma ótima faculdade.

#### Statement of Purpose (Até 5)
É a coluna que trata da carta de intenção, um documento formal que expressa o interesse de um candidato em uma oportunidade, como uma vaga de emprego ou um curso acadêmico, destacando suas motivações e qualificações.

#### Letter of Recomendation (Até 5)
É a coluna que trata da carta de recomendação, um documento que atesta as habilidades e qualidades de um candidato, geralmente escrito por um ex-supervisor, professor ou colega, com o objetivo de apoiar sua candidatura a uma vaga de emprego ou estudo.

#### Undergraduate GPA (Até 4)
É a coluna que trata do histórico escolar do aluno.

#### Research (0 ou 1)
É a coluna que trata se o aluno teve trabalhos extracurriculares, por exemplo pesquisa.

#### Chance of Admit (Variando de 0 a 1)
É a coluna que fala se o aluno tem chance de ser aprovado ou não, mediante suas características anteriores.

## Modelo

### Realização do modelo
![Árvore de decisão](https://raw.githubusercontent.com/leonamcassemir0/portfolio/main/arvore-de-decisao.gif)

Para rodar o algoritmo da árvore de decisão, tive que tratar as colunas 'GRE Score' e 'TOEFL Score' com a função *StandardScaler* da biblioteca Scikit-Learn, pois elas tinham dados que estavam fora de escala com as outras colunas, o que faz  o modelo performar mal.

Além disso, para que o modelo seja treinado, nossa coluna target ('Chance of Admit') deve ser uma coluna dummy(0 ou 1). Então, para isso, criei uma coluna nova chamada 'Aprovado' que atribui 1(aprovado) para o aluno que obteve porcentagem maior ou igual a 60% na coluna 'Chance of admit' e 0(Reprovado) para quem obteve abaixo de 60%.

### Treinamento do modelo
Para treinar o modelo resolvi pegar 70% dos dados, porque por se tratar de um dataset pequeno, quis deixar um pouco mais de dados para testar e melhorar o modelo.

## Avaliação
![Categoricas](https://raw.githubusercontent.com/leonamcassemir0/portfolio/main/OIP.webp)

Após o modelo treinado e testado, utilizei as principais métricas de avaliação de modelos de classificação. Nosso modelo teve um bom Recall e Precision, ambos com 95% e uma acurácia de 91%! Além disso nossa matriz de confusão ficou assim:

|          | Positivo | Negativo |
|----------|----------|----------|
| **Positivo** | 13       | 12       |
| **Negativo** | 14       | 261      | 

## Conclusão

![Categoricas](https://raw.githubusercontent.com/leonamcassemir0/portfolio/main/nice-smack.gif)

Como um dos meus primeiros modelos criados sozinho, gostei bastante dele. Como pode ver, é um modelo básico, mas com muito aprendizado.
Aprendi a como implementar uma árvore de decisão, como tratar dados discrepantes, como analisar colunas e como utilizar as principais bibliotecas para realizar o modelo da melhor forma possível. Fique à vontade para ver o notebook e analisar o código digitado, até mais! 

## Autor

Este projeto foi desenvolvido por Leonam Cassemiro, estudante de ciência de dados e engenharia de software. Críticas construtivas são sempre bem-vindas para aprimoramento contínuo.

* [LinkedIn](www.linkedin.com/in/leonam-cassemiro)
  
* [GitHub](https://github.com/leonamcassemir0)

* [Instagram](https://www.instagram.com/leonam.ds)

