# Classificação de Gênero de Voz por Inteligência Artificial

## Integrante
Arthur Chiarato Gorini Gomes RA: 23016363-2

## 1. Contextualização
A IA está presente em diversas aplicações que utilizam reconhecimento de voz. Neste trabalho foi desenvolvido um sistema capaz de identificar se uma voz pertence a uma pessoa do sexo masculino ou feminino utilizando técnicas de aprendizado de máquina.

## 2. Problema
Classificar vozes masculinas e femininas a partir de características numéricas extraídas de gravações de áudio.

## 3. Hipótese
A hipótese inicial era que o algoritmo SVM apresentaria melhor desempenho na classificação das vozes.

## 4. Dataset Utilizado
* **Nome do Dataset:** Voice Gender Recognition Dataset
* **Origem:** O dataset foi obtido na plataforma Kaggle, amplamente utilizada para compartilhamento de bases de dados voltadas ao aprendizado de máquina e ciência de dados.
* **Quantidade de Registros:** O conjunto de dados é composto por:
  * 3168 amostras de voz;
  * 1584 vozes masculinas;
  * 1584 vozes femininas.
  * *Dessa forma, o dataset encontra-se balanceado entre as duas classes.*
* **Variável Alvo:** A variável alvo utilizada foi `label`.
  * **Possíveis valores:** `male` (masculino) / `female` (feminino).

## 5. Preparação dos Dados
Antes do treinamento dos modelos, foram realizadas as seguintes etapas:
* Leitura do dataset utilizando a biblioteca Pandas;
* Análise exploratória dos dados;
* Conversão da variável alvo para formato numérico utilizando `LabelEncoder`;
* Separação dos atributos e da variável alvo;
* Divisão dos dados em conjuntos de treinamento e teste;
* Normalização dos atributos utilizando `StandardScaler`.

A divisão utilizada foi de:
* **70%** dos dados para treinamento;
* **30%** dos dados para teste.

## 6. Métodos Utilizados
### KNN (K-Nearest Neighbors)
O algoritmo KNN realiza a classificação de novas amostras com base nos exemplos mais próximos presentes no conjunto de treinamento. Neste trabalho foi utilizado o valor de K igual a 5, ou seja, cada previsão foi realizada considerando os cinco vizinhos mais próximos.
*Este método representa um algoritmo estudado na Parte 1 da disciplina.*

### SVM (Support Vector Machine)
O algoritmo SVM busca encontrar a melhor fronteira de separação entre as classes, denominada hiperplano. Seu objetivo é maximizar a distância entre as diferentes categorias, aumentando a capacidade de generalização do modelo.
*Este método representa um algoritmo estudado na Parte 2 da disciplina.*

## 7. Resultados Obtidos
Após o treinamento e avaliação dos modelos, foram obtidos os seguintes resultados:

| Modelo | Acurácia |
| :--- | :--- |
| **KNN** | 97,37% |
| **SVM** | 97,06% |

Os dois algoritmos apresentaram desempenho elevado, demonstrando grande capacidade de classificação para o problema proposto.

## 8. Análise dos Resultados
Os resultados demonstraram que ambos os modelos foram capazes de identificar corretamente vozes masculinas e femininas com alta precisão.
Apesar da hipótese inicial indicar que o SVM apresentaria melhor desempenho, o KNN obteve a maior acurácia, alcançando 97,37%, enquanto o SVM atingiu 97,06%.
A diferença entre os modelos foi pequena, mostrando que ambos são adequados para problemas de classificação envolvendo características numéricas extraídas de sinais de áudio.

## 9. Conclusão
O desenvolvimento deste projeto permitiu aplicar na prática conceitos estudados durante a disciplina de Inteligência Artificial, incluindo preparação de dados, treinamento, avaliação e comparação de modelos.
Os resultados mostraram que tanto o KNN quanto o SVM são capazes de realizar a classificação de vozes masculinas e femininas com excelente desempenho. Embora o KNN tenha apresentado a maior acurácia neste conjunto de dados, a diferença em relação ao SVM foi pequena.
Dessa forma, conclui que os atributos numéricos extraídos das gravações de áudio fornecem informações suficientes para que algoritmos de aprendizado de máquina realizem a classificação de gênero de voz de maneira eficiente e confiável.
