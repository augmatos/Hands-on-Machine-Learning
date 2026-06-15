# 📘 Hands-on Machine Learning

> Implementações práticas dos capítulos do livro *Hands-on Machine Learning with Scikit-Learn, Keras & TensorFlow* — Aurélien Géron

---

## 📌 Sobre o Projeto

Este repositório reúne meus estudos e implementações baseados no livro **"Hands-on Machine Learning with Scikit-Learn, Keras & TensorFlow"** de Aurélien Géron. Cada notebook cobre um capítulo do livro com implementações, experimentos e anotações em português.

O foco é aprendizado prático: entender os algoritmos implementando-os, visualizando resultados e analisando o comportamento dos modelos com dados reais.

---

## 📓 Notebooks

| # | Notebook | Tópico | Algoritmos/Conceitos |
|---|----------|--------|----------------------|
| 02 | [End-to-End ML Project](02_end_to_end_machine_learning_project.ipynb) | Projeto completo ponta a ponta | Pipeline, EDA, RandomForest, GridSearchCV |
| 03 | [Classification](03_classification.ipynb) | Classificação | SGD, Confusion Matrix, ROC, Precision/Recall |
| 04 | [Training Linear Models](04_training_linear_models.ipynb) | Modelos Lineares | Regressão Linear, Ridge, Lasso, Logística, SGD |
| 05 | [Support Vector Machines](05_support_vector_machines.ipynb) | SVMs | SVC Linear, Kernel RBF, Polynomial, SVR |
| 06 | [Decision Trees](06_decision_trees.ipynb) | Árvores de Decisão | CART, Regularização, Instabilidade |
| 08 | [Dimensionality Reduction](08_dimensionality_reduction.ipynb) | Redução de Dimensionalidade | PCA, Kernel PCA, LLE, t-SNE |
| 09 | [Unsupervised Learning](09_unsupervised_learning.ipynb) | Aprendizado Não Supervisionado | K-Means, DBSCAN, GMM, Detecção de Anomalias |

---

## 🗂️ Datasets Utilizados

| Dataset | Capítulo | Descrição |
|---------|----------|-----------|
| **California Housing** | Cap. 02 | Preço de imóveis na Califórnia — problema de regressão |
| **MNIST** | Cap. 03 | Reconhecimento de dígitos manuscritos — classificação multiclasse |
| **Titanic** | Cap. 03 | Sobrevivência no naufrágio — classificação binária |
| **Iris** | Cap. 04, 06 | Classificação de espécies de flores |
| **Moons / Blobs** | Cap. 05, 09 | Dados sintéticos para benchmark de algoritmos |

---

## 🚀 Como Executar

### Pré-requisitos

```bash
pip install scikit-learn numpy pandas matplotlib jupyter
```

### Rodando localmente

```bash
git clone https://github.com/augmatos/Hands-on-Machine-Learning.git
cd Hands-on-Machine-Learning
jupyter notebook
```

### Google Colab

Cada notebook pode ser aberto diretamente no Colab via o badge no início do arquivo.

---

## 🛠️ Tecnologias

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

---

## 📚 Conceitos Cobertos por Capítulo

### Cap. 02 — Projeto Ponta a Ponta
- Análise Exploratória de Dados (EDA)
- Feature Engineering e transformações
- Pipelines de pré-processamento
- Cross-validation e Fine-tuning com GridSearchCV
- Random Forest e avaliação de modelos

### Cap. 03 — Classificação
- Classificadores binários e multiclasse
- Métricas: Precision, Recall, F1-Score, ROC-AUC
- Matriz de confusão e análise de erros
- One-vs-All e One-vs-One
- Classificação multilabel

### Cap. 04 — Modelos Lineares
- Regressão Linear (Equação Normal e Gradiente Descendente)
- Gradiente Descendente Estocástico (SGD)
- Regressão Polinomial
- Regularização: Ridge, Lasso, Elastic Net
- Regressão Logística e Softmax

### Cap. 05 — Máquinas de Vetores de Suporte (SVM)
- SVM de Margem Larga (Hard e Soft Margin)
- Kernel Trick: Polinomial e RBF (Gaussiano)
- SVM para Regressão (SVR)

### Cap. 06 — Árvores de Decisão
- Algoritmo CART
- Visualização de árvores
- Regularização (max_depth, min_samples_leaf)
- Instabilidade e sensibilidade a rotações

### Cap. 08 — Redução de Dimensionalidade
- PCA e variância explicada
- Kernel PCA (não-linear)
- Locally Linear Embedding (LLE)
- t-SNE para visualização

### Cap. 09 — Aprendizado Não Supervisionado
- K-Means e inicialização K-Means++
- Silhouette Score e Elbow Method
- DBSCAN
- Gaussian Mixture Models (GMM)
- Detecção de anomalias e novidades

---

## 📈 Status dos Notebooks

| Notebook | Status |
|----------|--------|
| Cap. 02 — End-to-End Project | ✅ Completo |
| Cap. 03 — Classification | ✅ Completo |
| Cap. 04 — Linear Models | ✅ Completo |
| Cap. 05 — SVM | ✅ Completo |
| Cap. 06 — Decision Trees | ✅ Completo |
| Cap. 07 — Ensemble Learning | 🔄 Em desenvolvimento |
| Cap. 08 — Dimensionality Reduction | ✅ Completo |
| Cap. 09 — Unsupervised Learning | ✅ Completo |

---

## 📖 Referência

> Géron, Aurélien. *Hands-on Machine Learning with Scikit-Learn, Keras, and TensorFlow*. O'Reilly Media, 2019.
>
> [GitHub oficial do livro](https://github.com/ageron/handson-ml2)

---

## 👨‍💻 Autor

**Augusto Matos** — Analista de Dados & Desenvolvedor Python

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/augusto-matos-b92887204)
[![Outlook](https://img.shields.io/badge/Outlook-0078D4?style=for-the-badge&logo=microsoft-outlook&logoColor=white)](mailto:augusto.ivan83@outlook.com)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/augmatos)

---

## 📝 Licença

Projeto de código aberto para fins educacionais. Os notebooks são baseados no material do livro de Aurélien Géron.
