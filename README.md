Classificação de Partículas: Telescópio MAGIC Gamma 

Este projeto utiliza técnicas de Machine Learning para classificar partículas detectadas pelo telescópio terrestre de raios gama MAGIC (Major Atmospheric Gamma Imaging Cherenkov). O objetivo é distinguir entre sinais de raios gama (sinal) e ruído de fundo hadrônico (background).

Objetivo do Projeto: 

Desenvolver um modelo preditivo capaz de realizar a classificação binária de eventos de partículas com alta precisão, comparando diferentes algoritmos de aprendizado de máquina para identificar o melhor equilíbrio entre desempenho e tempo de processamento.

O Dataset:

O conjunto de dados utilizado foi o magic04.data, que consiste em:

- 19.020 instâncias totais.

- 10 variáveis preditivas (características físicas da imagem da partícula).

- Variável alvo: 'g' para sinal (gamma) e 'h' para fundo (hadron).

Pré-processamento:

- Transformação de Dados: Conversão da variável alvo para formato binário (0 e 1).

- Escalonamento: Utilização do StandardScaler para normalizar as grandezas das variáveis.

- Tratamento de Desbalanceamento: Aplicação do RandomOverSampler para equilibrar as classes no conjunto de treinamento.

Tecnologias Utilizadas:

- Python 3.x

Bibliotecas:

- Pandas e NumPy para manipulação de dados.

- Matplotlib e Seaborn para visualização e análise exploratória.

- Scikit-learn para algoritmos de ML e métricas.

- TensorFlow/Keras para implementação da Rede Neural.

Modelos Implementados e Resultados:

Foram testados cinco algoritmos diferentes. Abaixo, o resumo do desempenho observado:

| Modelo | Acurácia | Tempo de Inferência |
| :--- | :---: | :---: |
| **Neural Network** | **87.9%** | 0.258s |
| **SVM** | 87.4% | 1.284s |
| **K-Nearest Neighbors (KNN)** | 81.7% | 0.227s |
| **Logistic Regression** | 78.3% | 0.001s |
| **Naive Bayes** | 73.0% | 0.001s |

Conclusões:

A Rede Neural e o SVM apresentaram os melhores resultados em termos de acurácia. No entanto, para aplicações que exigem respostas em tempo real, modelos como Regressão Logística podem ser preferíveis devido à rapidez quase instantânea de predição.

Como rodar este projeto localmente:

1. Clone o repositório: git clone https://github.com/seu-usuario/nome-do-repositorio.git

2. Certifique-se de ter as bibliotecas instaladas: pip install pandas scikit-learn tensorflow imbalanced-learn matplotlib

3. Abra o arquivo .ipynb no Jupyter Notebook ou VS Code.


Desenvolvido por: Diego Augusto Soares Amaral
