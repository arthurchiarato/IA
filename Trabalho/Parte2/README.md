# Classificação de Vozes Masculinas e Femininas utilizando KNN e SVM

## Integrantes
- Arthur Gorini

## Contextualização
A Inteligência Artificial está presente em diversas aplicações que utilizam reconhecimento de voz. Neste trabalho foi desenvolvido um sistema capaz de identificar se uma voz pertence a uma pessoa do sexo masculino ou feminino utilizando técnicas de aprendizado de máquina.

## Problema
Classificar vozes masculinas e femininas a partir de características numéricas extraídas de gravações de áudio.

## Hipótese
A hipótese inicial era que o algoritmo SVM apresentaria melhor desempenho na classificação das vozes.

## Dataset Utilizado
### Nome
Voice Gender Recognition Dataset

### Origem
Kaggle

### Quantidade de Registros
- 3168 amostras
- 1584 vozes masculinas
- 1584 vozes femininas

### Variável Alvo
label (male / female)

## Preparação dos Dados
1. Leitura do dataset
2. Análise exploratória
3. LabelEncoder
4. Divisão treino/teste
5. Normalização com StandardScaler

## Métodos Utilizados

### KNN
Método da Parte 1 da disciplina.

### SVM
Método da Parte 2 da disciplina.

## Resultados

| Modelo | Acurácia |
|----------|----------|
| KNN | 97,37% |
| SVM | 97,06% |

## Conclusão
Os dois modelos apresentaram desempenho superior a 97% de acurácia. O KNN obteve o melhor resultado, mas a diferença para o SVM foi pequena.
