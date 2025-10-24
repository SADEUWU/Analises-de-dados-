# 📘 Teorema do Limite Central — Simulação e Visualização em R

Este projeto apresenta uma simulação completa do **Teorema do Limite Central (TLC)** utilizando a linguagem **R**, com o objetivo de demonstrar empiricamente como a **distribuição das médias amostrais** se aproxima de uma **distribuição normal**, mesmo quando a **população original não é normal**.

---

## 🎯 Objetivo do estudo

Comprovar, por meio de simulação computacional, que:
- A média das amostras tende à média populacional (μ);
- O desvio-padrão das médias segue a relação teórica σ/√n;
- À medida que o tamanho da amostra (n) aumenta, a forma da distribuição das médias amostrais se torna normal.

---

## 🧩 Estrutura do trabalho

### 🔹 **Experimento 1 — Distribuições Normais**
- Definição e plotagem das funções densidade de probabilidade (fdp) de três variáveis normais:
  - X ~ N(90, 100)
  - Y ~ N(90, 80)
  - Z ~ N(85, 100)
- Comparação gráfica das curvas para entender os efeitos da média e do desvio-padrão.

### 🔹 **Experimento 2 — Teorema do Limite Central**
- Simulação de várias amostras de uma **população exponencial (não normal)**.
- Cálculo das médias amostrais para diferentes tamanhos de amostra:
  - n = 100
  - n = 10.000
  - n = 1.000.000
- Construção dos histogramas das médias amostrais.
- Comparação com a curva normal teórica.

---

## 📊 Resultados principais

| n | repetições | média das médias | sd empírico | sd teórico | dentro ±1σ | dentro ±2σ | dentro ±3σ |
|---|-------------|------------------|--------------|-------------|-------------|-------------|-------------|
| 100 | 1.000 | 4.9873 | 0.489 | 0.500 | 69.2% | 95.5% | 99.8% |
| 10.000 | 200 | 4.9977 | 0.046 | 0.050 | 65.5% | 96.0% | 100.0% |
| 1.000.000 | 20 | 4.9989 | 0.004 | 0.005 | 70.0% | 100.0% | 100.0% |

➡️ **Conclusão:**  
Conforme o tamanho da amostra cresce, o desvio-padrão das médias diminui proporcionalmente a σ/√n e a distribuição das médias se torna praticamente normal, mesmo com população não normal.

---

## 🧠 Conclusão geral

Foram realizadas simulações com tamanhos de amostra n = 100, 10.000 e 1.000.000, com médias populacionais μ = 5 e distribuição exponencial original.  
Observou-se que o aumento do tamanho amostral reduziu significativamente o desvio-padrão das médias e fez com que a distribuição das médias amostrais se tornasse cada vez mais simétrica e semelhante à curva normal teórica.  
As proporções de dados dentro de ±1, ±2 e ±3 desvios-padrão aproximaram-se dos valores esperados para a normal (68%, 95%, 99%), e a presença de outliers praticamente desapareceu.  
O gráfico apresentado ilustra visualmente o Teorema do Limite Central, mostrando que a média amostral se concentra em torno da média populacional (μ), com variabilidade decrescente proporcional a σ/√n, validando o comportamento previsto pelo Teorema do Limite Central.

---

## 🧾 Referências

- BUSSAB, W. O.; MORETTIN, P. A. *Estatística Básica*. 9ª ed. São Paulo: Saraiva, 2023.  
- MAGALHÃES, M. N.; LIMA, A. C. P. *Noções de Probabilidade e Estatística*. 8ª ed. São Paulo: Editora da Universidade de São Paulo, 2020.  
- R Core Team (2025). *R: A Language and Environment for Statistical Computing*.  
