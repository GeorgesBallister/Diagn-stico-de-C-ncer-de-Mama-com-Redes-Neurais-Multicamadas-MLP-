
---

# Equipe de Machine Learning

## Diagnóstico de Câncer de Mama com Redes Neurais Multicamadas (MLP)

---

## Contexto

O diagnóstico precoce do câncer de mama é crucial para o sucesso do tratamento e a redução da mortalidade. Este projeto aborda o problema da **classificação de tumores mamários (benigno vs. maligno)** utilizando **Redes Neurais Multicamadas (MLP)**. Nosso objetivo é desenvolver um modelo robusto e preciso que possa auxiliar profissionais de saúde na tomada de decisões, contribuindo para diagnósticos mais rápidos e confiáveis. A aplicação de técnicas de Machine Learning, em particular redes neurais, tem se mostrado promissora para extrair padrões complexos de dados médicos e oferecer suporte clínico.

---

## Integrantes da Equipe

- Danilo Melo
- Kássio Fonseca
- Romulo Galdino
- Georges B
---

## Base de Dados

O dataset utilizado para este projeto é o **"Breast Cancer Wisconsin (Diagnostic) Dataset"**, disponível no repositório UCI Machine Learning.

**Link:** [https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic](https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic)

Este dataset contém características computadas a partir de uma imagem digitalizada de um aspirado por agulha fina (FNA) de uma massa mamária. Ele descreve características dos núcleos celulares presentes na imagem, como raio, textura, perímetro, área, suavidade, compactação, concavidade, pontos côncavos, simetria e dimensão fractal. O objetivo é classificar se o tumor é **benigno (B)** ou **maligno (M)**.

---

## Ferramentas e Versões

- **Python:** 3.x
- **TensorFlow:** 2.x
- **Keras:** (integrado ao TensorFlow 2.x)
- **scikit-learn:** 1.x
- **ucimlrepo:** 0.0.x (para fácil acesso aos datasets do UCI)
- **NumPy:** 1.x
- **Matplotlib:** 3.x

---

## Link para o Notebook Colab

[https://colab.research.google.com/drive/1Y4RTfwF52dgE2S7y2CQ-lNBkW8ceoh5c?usp=sharing](https://colab.research.google.com/drive/1Y4RTfwF52dgE2S7y2CQ-lNBkW8ceoh5c?usp=sharing)

---

## Descrição Breve

Este projeto implementa e avalia uma **Rede Neural Multicamadas (MLP)** para a classificação de casos de câncer de mama como benignos ou malignos, utilizando o Breast Cancer Wisconsin (Diagnostic) Dataset. O código explora desde a carga e pré-processamento dos dados (padronização e one-hot encoding), até a construção, treinamento e avaliação do modelo MLP.

A arquitetura final da MLP conta com **duas camadas ocultas**, utilizando funções de ativação **ReLU**. Para otimização e prevenção de overfitting, foram aplicadas técnicas como **regularização L2** (para penalizar pesos grandes), **Dropout** (para desativar neurônios aleatoriamente durante o treinamento) e **Early Stopping** (para interromper o treinamento quando não há mais melhoria na acurácia de validação). Além disso, foram calculados e aplicados **pesos de classe** para lidar com possíveis desequilíbrios, garantindo que o modelo não seja enviesado para a classe majoritária.

O modelo é compilado com o otimizador **Adam** e a função de perda **`categorical_crossentropy`**, sendo avaliado principalmente pela **acurácia**. Os resultados são apresentados com a acurácia final do modelo no conjunto de teste, e gráficos da perda de treinamento e validação ao longo das épocas são gerados para visualização do processo de aprendizado e identificação de overfitting.

---
