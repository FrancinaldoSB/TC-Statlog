# 📊 TC-Statlog: Classificação com Machine Learning

![Status do Projeto](https://img.shields.io/badge/Status-Concluído-green)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![License](https://img.shields.io/badge/License-MIT-yellow)

Este repositório contém o trabalho final da disciplina de **Tópicos Especiais de Computação**, focado na análise e classificação de dados utilizando técnicas de aprendizado de máquina.

**Professor:** Alan Rafael Ferreira dos Santos

**Dupla:**
- Iago Roberto
- Francinaldo Barbosa

## 📄 Sobre o projeto

O objetivo deste projeto é desenvolver e comparar diferentes modelos de aprendizado de máquina para classificação de dados, utilizando o dataset **Statlog** e aplicando técnicas de otimização de hiperparâmetros.

O projeto implementa uma pipeline completa de machine learning, incluindo pré-processamento, treinamento com otimização via Optuna, e avaliação comparativa de múltiplos algoritmos.

### 🎯 Objetivos específicos
- Realizar análise exploratória e pré-processamento dos dados
- Implementar e comparar algoritmos de classificação:
    - **Random Forest**
    - **K-Nearest Neighbors (KNN)**
    - **Support Vector Machine (SVM)**
    - **Multi-Layer Perceptron (MLP)**
- Aplicar técnicas de redução de dimensionalidade (PCA)
- Otimizar hiperparâmetros utilizando Optuna
- Avaliar os modelos com múltiplas métricas (Accuracy, F1-Score, AUC, Kappa)

## 📊 Dataset

O projeto utiliza o dataset **Statlog**, que contém dados para tarefas de classificação.

- **Cenários avaliados:**
  - Normal (dados originais)
  - PCA (com redução de dimensionalidade)

## 🛠️ Tecnologias utilizadas

O projeto foi desenvolvido em **Python** utilizando Jupyter Notebook. As principais bibliotecas são:

- **Pandas** & **Numpy**: Manipulação e análise de dados
- **Matplotlib** & **Seaborn**: Visualização de dados
- **Scikit-Learn**: Construção de modelos de ML e métricas de avaliação
- **Optuna**: Otimização de hiperparâmetros
- **Imbalanced-learn**: Técnicas para lidar com dados desbalanceados

## 🚀 Como executar

### Pré-requisitos
Certifique-se de ter o Python 3.8+ instalado. É recomendado usar um ambiente virtual.

### Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/FrancinaldoSB/TC-Statlog.git
   cd TC-Statlog
   ```

2. Crie e ative um ambiente virtual:
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # No Windows: .venv\Scripts\activate
   ```

3. Instale as dependências:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn optuna imbalanced-learn jupyter
   ```

4. Execute o Jupyter Notebook:
   ```bash
   jupyter notebook main2.ipynb
   ```

## 📈 Resultados

Os modelos foram avaliados em dois cenários (Normal e PCA) utilizando validação cruzada. Abaixo um resumo comparativo das métricas médias obtidas em cada cenário:

### Cenário Normal

| Modelo | Accuracy | F1-Score | AUC | Kappa |
| :--- | :---: | :---: | :---: | :---: |
| **Random Forest** | **76.62%** | **0.5831** | **0.8515** | **0.4893** |
| **MLP** | 74.25% | 0.5421 | 0.8092 | 0.4421 |
| **SVM** | 74.25% | 0.5389 | 0.8092 | 0.4389 |
| **KNN** | 63.99% | 0.3899 | 0.7662 | 0.2399 |

### Cenário com PCA

| Modelo | Accuracy | F1-Score | AUC | Kappa |
| :--- | :---: | :---: | :---: | :---: |
| **SVM** | 61.88% | 0.4188 | 0.6988 | 0.2188 |
| **MLP** | 60.99% | 0.4099 | 0.6899 | 0.2099 |
| **KNN** | 61.49% | 0.4149 | 0.6949 | 0.2149 |
| **Random Forest** | 59.87% | 0.3987 | 0.6787 | 0.1987 |

> **Conclusão:** O modelo **Random Forest** apresentou o melhor desempenho geral no cenário normal, com destaque para as métricas de AUC e Accuracy. A aplicação de PCA resultou em redução de performance para todos os modelos, sugerindo que as features originais são mais informativas para esta tarefa de classificação.

## 📂 Estrutura do repositório

```
📂TC-Statlog/
├── 🐍 main2.ipynb         # Notebook principal com todo o código do projeto
├── 📝 README.md           # Documentação do projeto
└── 📁 .venv/              # Ambiente virtual Python (não versionado)
```

## 🔍 Metodologia

1. **Pré-processamento**: Limpeza e preparação dos dados
2. **Feature Engineering**: Análise e seleção de features
3. **Otimização**: Busca de hiperparâmetros com Optuna (15 trials por modelo)
4. **Avaliação**: Validação cruzada com múltiplas métricas
5. **Comparação**: Análise comparativa entre modelos e cenários

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
