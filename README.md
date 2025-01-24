
# 🩺 **Machine Learning na Análise Clínica da Tuberculose**
![img](/img/fig2.png)

*Figura 1: Metodologia utilizada no projeto para análise de dados clínicos relacionados à tuberculose.*

---

## ✨ **Descrição do Projeto**
Este projeto aplica **Machine Learning** na análise de dados clínicos relacionados à tuberculose. O objetivo principal é identificar padrões, realizar classificações e agrupar pacientes de forma eficiente. A metodologia consiste em diversas etapas: pré-processamento, análise exploratória, clusterização e construção de modelos preditivos para auxílio no diagnóstico da doença.

---

## 📊 **Principais Etapas e Implementações**

### 1. **Pré-processamento e Limpeza dos Dados**  
   - Exclusão de colunas irrelevantes como `testesensibilidade` e variáveis altamente desbalanceadas.
   - Tratamento de valores ausentes, substituindo-os por valores como `Nulo`.
   - Geração de variáveis dummies para dados categóricos, como `sexo`.

### 2. **Análise Exploratória de Dados (EDA)**  
   - Geração de relatórios com **pandas-profiling** para identificação de tendências e problemas nos dados.
   - Mapas de calor de correlações utilizando a biblioteca **seaborn**.
   - Identificação de variáveis significativas por meio do teste qui-quadrado.

### 3. **Clusterização**  
   - Aplicação de **K-Means**, **MiniBatchKMeans** e **KModes** para agrupamento.
   - Redução de dimensionalidade com **PCA** e **MCA** para melhor visualização.
   - Análise detalhada de cada cluster, incluindo proporção de pacientes diagnosticados.

**Figura 2: Visualização dos Clusters após MCA.**
![img](/img/fig1.png)

### 4. **Modelagem Preditiva**  
   - Modelos testados:
     - **Random Forest**
     - **AdaBoost**
     - **Logistic Regression**
     - **XGBoost**
     - **SVM**
   - Otimização dos hiperparâmetros com **Optuna** para maximizar a acurácia e outras métricas.
   - Avaliação dos modelos com métricas como **Accuracy**, **ROC-AUC**, **F1-Score**, e **Recall**.

### 5. **Análise de Importância das Variáveis**  
   - Identificação de variáveis mais relevantes usando **SHAP** e **Feature Importance**.
   - Visualização dos impactos das variáveis no modelo com gráficos de swarm e waterfall.

**Figura 3: Avaliação de Correlação**
![img](/img/fig3.png)

### 6. **Validação e Comparação de Modelos**  
   - **LazyPredict** foi utilizado para uma análise inicial de desempenho dos modelos.
   - Modelos foram comparados com base em suas métricas, e os resultados armazenados em arquivos Excel.

**Figura 4: Matriz de Confusão de um dos Modelos.**
![img](/img/fig4.png)

---

## 📂 **Estrutura do Projeto**

```plaintext
├── Dataset/
│   └── datasetTB4.csv
├── EDA/
│   └── tuberculosis_analysis.html
│   └── Tuberculosis_Clusters_Comparison.html
├── Results/
│   └── models_results.xlsx
├── Notebooks/
│   └── minib_kmeans_and_model_predict.ipynb
├── Imagens/
│   └── fig1.png
│   └── fig2.png
│   └── fig3.png (Metodologia)
│   └── fig4.png
```

---

## ⚙️ **Requisitos**

- **Python 3.7+**
- Bibliotecas:
  - `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `optuna`, `shap`
  - Outros detalhados no arquivo `requirements.txt`.

---

## 🚀 **Como Executar**

1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   ```
2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
3. Execute o notebook:
   ```bash
   jupyter notebook Notebooks/minib_kmeans_and_model_predict.ipynb
   ```

---

## 📈 **Resultados e Visualizações**

### 🧪 **Clusterização**
- Utilizamos os algoritmos **K-Means** e **KModes** para agrupar pacientes.  
- Os clusters foram visualizados em gráficos 2D após redução dimensional com **PCA** e **MCA**.

### 📊 **Importância das Variáveis**
- Avaliação das features mais relevantes para o diagnóstico com técnicas de seleção e interpretação.

### 🔍 **Resultados dos Modelos**
- Modelos como **AdaBoost**, **Random Forest** e **XGBoost** foram otimizados e avaliados.  
- Os melhores resultados foram armazenados em um relatório Excel.

---

## 📜 **Metodologia**

A metodologia é representada na **Figura 1** acima. As principais etapas incluem:
- **Pré-processamento:** Limpeza e normalização dos dados.
- **Clusterização:** Agrupamento de pacientes para identificação de padrões.
- **Modelagem:** Construção e validação de modelos para previsão de resistência à tuberculose.

---


**Contribuição:**  
Caso deseje contribuir com melhorias, sinta-se à vontade para abrir um pull request. Feedbacks são sempre bem-vindos! 😊
