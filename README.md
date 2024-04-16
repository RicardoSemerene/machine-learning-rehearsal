<center>
  <h1>Ensaios de Machine Learning</h1>
</center>

<center>

![imagem](img.jpg)

</center>

---

# 1. Contexto

A empresa Data Money fornece serviços de consultoria de Análise e Ciência de Dados para grandes empresas no Brasil e no exterior. O seu principal diferencial de mercado em relação aos concorrentes é o alto retorno financeiro para as empresas clientes, graças a performance de seus algoritmos de Machine Learning.

A Data Money acredita que a expertise no treinamento e ajuste fino dos algoritmos, feito pelos Cientistas de Dados da empresa, é a principal motivo dos ótimos resultados que as consultorias vem entregando aos seus clientes.

Para continuar crescendo a expertise do time, os Cientistas de Dados acreditam que é extremamente importante realizar ensaios nos algoritmos de Machine Learning para adquirir uma experiência cada vez maior sobre o seu funcionamento e em quais cenários as performances são máximas e mínimas, para que a escolha do algoritmo para cada situação seja a mais correta possível.

# 2. O Projeto

A respeito deste contexto, este projeto consiste em ensaios de Machine Learning utilizando modelos de Classificação, Regressão e Clusterização. Ressalta-se que, como o foco é trabalhar com os algortimos de Machine Learning, não é escopo deste trabalho a execução das outras etapas de um projeto tradicional de ciência de dados.   

# 3. Estratégia para Solução

De posse dos dados já preparados, a estratégia aqui é ensaiar 4 algoritmos de Machine Learning para problemas de Classificação. Nestes problemas, as métricas mais utilizadas pra medir a performance são: Accuracy, Precision, Recall e F1-Score. E os algoritmos trabalhados foram: KNN, Decision Tree, Random Forest e Logistic Regression.

Para a Regressão, mais ensaios foram realizados, pois utilizamos técnicas para regularização L1 (Lasso), L2 (Ridge) e L1 e L2 combinadas (Elastic Net). Portanto, os algortimos ensaiados foram: Linear Regression, Decision Tree Regressor, Random Forest Regressor, Polinomial Regression, Linear Regression Lasso, Linear Regression Ridge, Linear Regression Elastic Net, Polinomial Regression Lasso, Polinomial Regression Ridge e Polinomial Regression Elastic Net. Já as métricas para avaliar seus desempenhos foram: R2, MSE, RMSE, MAE e MAPE.

Na Clusterização, foram ensaiados dois algoritmos: K-Means e Affinity Propagation. E, apesar de fazer a análise com outras métricas, a métrica principal para agrupamentos é a Silhouette Score.

Ao final, foram construídas sete tabelas com as respectivas métricas para cada algoritmo, nos dados de treino, validação e teste para cada situação para os algoritmos de aprendizado supervisionado (Classificação e Regressão). Portanto, três tabelas pra cada. Na Clusterização, aprendizado não-supervisionado, apenas uma tabela gerada.

Além disso, os diferentes parâmetros de cada algoritmos também foram testados. Os resultados apresentados abaixo, mostram os melhores coeficientes para as métricas entre as melhores combinações de parâmetros.

# 4. Top 3 Insights 

### Insight 1.

A Decision Tree e a Random Forest tiveram desempenho de 100% na Classificação para os dados de treino e 94% para validação e teste, não acarretando necessariamente em uma tendência para o overfiting, pois a queda de desempenho não foi tão brusca. Ainda sobre o tipo de aprendizado supervisionado Classificação, os algoritmos baseados em árvore desempenharam melhor que os demais algoritmos. Geralmente, estes algortismos oferecem uma interpretabilidade maior do modelo. 

###  Insight 2. 

Na Regressão, com exceção da Decision Tree Regressor, para os dados de treino, em geral, os algoritmos não apresentaram um bom desempenho. Também para o treino, a Random Forest apresentou um desempenho satisfatório. O que não se confirmou nos dados de validação e teste, em que o RMSE entre todos os algoritmos esteve bem próximo. Se verifica a ocorrência de um overfiting, em que os modelos foram bem para dados conhecidos, mas muito ruins para outros dados, indicando uma capacidade ruim de generalização. 

### Insight 3. 

Na Clusterização, os dois algortimos tiveram performances muito próximas, porém valor baixo, proóximo de 0, para a Silhouette Score. Um valor mais próximo de 1 indica que dados estão bem agrupados e estão mais longe dos dados de outros clusters, o que é desejável. Um valor próximo de 0 indica que o dado pode ser pertencente a outro cluster, podendo ter a ocorrência até de sobreposição dos clusters, o que é totalmente indesejável. 

# 4. Resultados dos Ensaios

## 4.1 Classificação

### Dados de Treino

| Algoritmo           | Accuracy | Precision | Recall | F1-Score |
|---------------------|----------|-----------|--------|----------|
| KNN                 | 0.832    | 0.812     | 0.797  | 0.804    |
| Decision Tree       | 1        | 1         | 1      | 1        |
| Random Forest       | 1        | 1         | 1      | 1        |
| Logistic Regressor  | 0.793    | 0.729     | 0.831  | 0.777    |

### Dados de Validação

| Algoritmo           | Accuracy | Precision | Recall | F1-Score |
|---------------------|----------|-----------|--------|----------|
| KNN                 | 0.676    | 0.627     | 0.621  | 0.624    |
| Decision Tree       | 0.946    | 0.936     | 0.939  | 0.938    |
| Random Forest       | 0.965    | 0.975     | 0.943  | 0.959    |
| Logistic Regressor  | 0.794    | 0.731     | 0.831  | 0.778    |

### Dados de Teste

| Algoritmo           | Accuracy | Precision | Recall | F1-Score |
|---------------------|----------|-----------|--------|----------|
| KNN                 | 0.688    | 0.648     | 0.635  | 0.641    |
| Decision Tree       | 0.947    | 0.940     | 0.940  | 0.940    |
| Random Forest       | 0.946    | 0.937     | 0.941  | 0.939    |
| Logistic Regressor  | 0.641    | 0.629     | 0.442  | 0.520    |

## 4.2 Regressão

### Dados de Treino

| Algoritmo                         | R2    | MSE     | RMSE   | MAE    | MAPE    |
|-----------------------------------|-------|---------|--------|--------|---------|
| Linear Regression                 | 0.046 | 455.996 | 21.354 | 16.998 | 865.318 |
| Linear Regression Lasso           | 0.007 | 474.474 | 21.782 | 17.305 | 873.669 |
| Linear Regression Ridge           | 0.045 | 456.353 | 21.362 | 17.005 | 866.045 |
| Linear Regression Elastic Net     | 0.010 | 473.210 | 21.753 | 17.281 | 872.238 |
| Polinomial Regression             | 0.094 | 432.986 | 20.808 | 16.458 | 835.053 |
| Polinomial Regression Lasso       | 0.009 | 473.638 | 21.763 | 17.285 | 869.970 |
| Polinomial Regression Ridge       | 0.082 | 438.505 | 20.940 | 16.592 | 846.203 |
| Polinomial Regression Elastic Net | 0.011 | 472.677 | 21.741 | 17.263 | 868.908 |
| Decision Tree Regressor           | 0.991 | 3.940   | 1.985  | 0.214  | 8.262   |
| Random Forest Regressor           | 0.903 | 46.356  | 6.808  | 4.855  | 256.471 |

### Dados de Validação

| Algoritmo                         | R2    | MSE     | RMSE   | MAE    | MAPE    |
|-----------------------------------|-------|---------|--------|--------|---------|
| Linear Regression                 | 0.039 | 458.447 | 21.411 | 17.039 | 868.254 |
| Linear Regression Lasso           | 0.007 | 473.747 | 21.765 | 17.264 | 869.580 |
| Linear Regression Ridge           | 0.039 | 458.571 | 21.414 | 17.033 | 867.773 |
| Linear Regression Elastic Net     | 0.007 | 473.747 | 21.765 | 17.264 | 869.580 |
| Polinomial Regression             | 0.066 | 445.768 | 21.113 | 16.749 | 854.793 |
| Polinomial Regression Lasso       | 0.009 | 472.912 | 21.746 | 17.238 | 868.184 |
| Polinomial Regression Ridge       | 0.065 | 446.445 | 21.129 | 16.769 | 862.671 |
| Polinomial Regression Elastic Net | 0.011 | 472.073 | 21.727 | 17.217 | 867.863 |
| Decision Tree Regressor           | -0.303| 622.635 | 24.952 | 17.166 | 694.183 |
| Random Forest Regressor           | 0.333 | 318.159 | 17.837 | 12.976 | 700.275 |

### Dados de Teste

| Algoritmo                         | R2    | MSE     | RMSE   | MAE    | MAPE    |
|-----------------------------------|-------|---------|--------|--------|---------|
| Linear Regression                 | 0.051 | 461.988 | 21.493 | 17.144 | 853.135 |
| Linear Regression Lasso           | 0.005 | 484.429 | 22.009 | 17.498 | 873.581 |
| Linear Regression Ridge           | 0.050 | 462.353 | 21.502 | 17.143 | 855.746 |
| Linear Regression Elastic Net     | 0.007 | 483.096 | 21.979 | 17.143 | 855.746 |
| Polinomial Regression             | 0.090 | 443.041 | 21.048 | 16.720 | 824.246 |
| Polinomial Regression Lasso       | 0.008 | 482.824 | 21.973 | 17.456 | 875.607 |
| Polinomial Regression Ridge       | 0.080 | 447.688 | 21.158 | 16.824 | 837.279 |
| Polinomial Regression Elastic Net | 0.009 | 482.227 | 21.959 | 17.440 | 875.498 |
| Decision Tree Regressor           | -0.258| 612.577 | 24.750 | 17.038 | 612.432 |
| Random Forest Regressor           | 0.404 | 289.736 | 17.021 | 12.240 | 627.921 |

## 4.3 Clusterização

| Algoritmo           | Número de Clusters | Average Silhouete Score |
|---------------------|--------------------|-------------------------|
| K-Means             | 3                  | 0.233                   |
| Affinity Propagation| 3                  | 0.215                   |

# 5. Conclusões

Estes ensaios são muito importantes para entendimento de possíveis problemas que os resultados das métricas nos apresentam. Também entender quais parâmetros são mais usados pra cada algoritmo e como seus valores se movimentam. Com esses ensaios, foi possível constatar tendências para o overfitting e para o underfiting, além de concluir que nem sempre haverá um modelo que descreva o problema com qualidade, como por exemplo neste caso para a Regressão, em que seria mais adequado preparar melhor os dados ou construir novas features. O coeficiente de determinação R² é uma métrica interessante para avaliar como o modelo se ajusta aos dados. Um valor de 1 indica que o modelo se ajusta perfeitamente aos dados. Vim na Regressão que isso não aconteceu.

Em relação a Classificação, observamos uma tendência de queda nas pontuações de precisão ao passar dos dados de treinamento para os dados de teste. Isso é esperado, já que os modelos são treinados para maximizar o desempenho nos dados de treinamento e podem não se ajustar tão bem aos dados de teste. Os algoritmos baseados em árvore apresentaram forte tendência ao overfitting nos dados de treino, mas também tiveram ótimo desempenho na validação e teste, o que sugere que eles generalizam bem para novos dados, apesar do potencial overfitting nos dados de treinamento. O KNN pode ser mais suscetível a overfitting (devido à queda brusca no desempnho de treino pra validação e teste) enquanto o Logistic Regressor parece ter uma melhor capacidade de generalização para novos dados.

Para os algoritmos de Cluster, ambos tiveram performances muito próximas, porém valor baixo, proóximo de 0, para a Silhouette Score. Um valor próximo de 0 indica que os exemplos estão próximos da fronteira de decisão entre dois clusters ou que podem ser mal classificados. Então, pode-se concluir que nenhum destes algoritmos foram capazes de modelar o problema com os dados utilizados. 

# 6. Lições Aprendidas e Próximos Passos

Em projetos seguintes, além do que já foi feito, podem ser incrementados:

- Testar outros parâmetros para estes algoritmos de Machine Learning
- Testar outros algoritmos de Machine Learning a fim de melhor explicar os dados
- É importante trabalhar com dados com features bem alocadas e preparação bem executada anteriormente
- Praticar e aprimorar os conhecimentos em projetos completos de Ciência de Dados



