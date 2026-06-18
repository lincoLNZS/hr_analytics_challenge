# 📊 HR Analytics Challenge - Predição de Attrition de Funcionários

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![Dataset Size](https://img.shields.io/badge/Dataset-1M%20registros-blue)
![Python](https://img.shields.io/badge/Python-3.8%2B-green)
![Machine Learning](https://img.shields.io/badge/ML-Classification-red)

## 📋 Visão Geral do Projeto

Este é um **Trabalho de Conclusão de Disciplina** da disciplina **Machine Learning Aplicado**, focado em análise de dados de Recursos Humanos e previsão de attrition (saída) de funcionários.

O projeto utiliza o dataset **IBM HR Analytics Employee Attrition & Performance** para construir modelos de classificação que identifiquem funcionários com risco de deixar a empresa, permitindo ações proativas de retenção.

## 🎯 Objetivos

- **Prever attrition**: Identificar funcionários com alta probabilidade de sair da empresa
- **Entender padrões**: Descobrir quais variáveis têm maior impacto na attrition
- **Gerar insights**: Fornecer recomendações acionáveis para o departamento de RH
- **Comparar modelos**: Avaliar diferentes algoritmos de classificação

## 📊 Dataset

### Características Principais

| Atributo | Valor |
|----------|-------|
| **Total de Registros** | 1.000.000 |
| **Total de Features** | 35 |
| **Variável Alvo** | Attrition (Yes/No) |
| **Taxa de Attrition** | ~16% (desbalanceado) |
| **Tipo de Problema** | Classificação Binária |
| **Fonte** | IBM HR Analytics Dataset |

### Principais Variáveis

#### 📍 Demográficas
- Age, Gender, MaritalStatus, Education, EducationField

#### 💼 Profissionais
- Department, JobRole, JobLevel, BusinessTravel, OverTime
- DistanceFromHome, YearsAtCompany, YearsInCurrentRole

#### 💰 Compensação
- MonthlyIncome, DailyRate, HourlyRate, MonthlyRate
- PercentSalaryHike, StockOptionLevel

#### 😊 Satisfação & Bem-estar
- EnvironmentSatisfaction, JobSatisfaction
- RelationshipSatisfaction, WorkLifeBalance, JobInvolvement

#### 📈 Performance & Desenvolvimento
- PerformanceRating, TrainingTimesLastYear
- TotalWorkingYears, NumCompaniesWorked

## 🗂️ Estrutura do Repositório

```
hr_analytics_challenge/
├── aula_07.ipynb           # Notebook principal com análise e modelagem
├── README.md              # Este arquivo
├── LICENSE                # Licença MIT
└── data/                  # (Opcional) Dados do projeto
```

## 🚀 Como Executar

### Pré-requisitos
- Python 3.8 ou superior
- Jupyter Notebook ou JupyterLab
- Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

### Instalação

```bash
# Clone ou acesse o repositório
cd hr_analytics_challenge

# Instale as dependências (se necessário)
pip install pandas numpy scikit-learn matplotlib seaborn

# Abra o notebook
jupyter notebook aula_07.ipynb
# ou
jupyter lab aula_07.ipynb
```

### Execução
1. Abra o arquivo `aula_07.ipynb`
2. Execute as células na ordem para:
   - Carregar e explorar os dados
   - Realizar análises exploratórias (EDA)
   - Preprocessar as variáveis
   - Treinar modelos de classificação
   - Avaliar e comparar resultados

## 📈 Análise Exploratória (EDA)

O notebook inclui:
- ✅ Distribuição das variáveis
- ✅ Análise de correlação com attrition
- ✅ Identificação de variáveis constantes (removidas)
- ✅ Visualizações dos padrões principais
- ✅ Análise de desbalanceamento de classes

## 🤖 Modelagem

### Variáveis Removidas
- `EmployeeCount` (constante = 1)
- `Over18` (constante = 'Y')
- `StandardHours` (constante = 80)
- `EmployeeNumber` (ID, sem valor preditivo)

### Variáveis Features Engineered
- Razões entre variáveis numéricas
- Normalizações de renda/experiência
- Interações entre features relevantes

### Algoritmos Testados
- Logistic Regression
- Decision Trees
- Random Forest
- Gradient Boosting (XGBoost/LightGBM)
- Support Vector Machines (SVM)

### Métricas de Avaliação
- Acurácia
- Precisão, Recall, F1-Score
- ROC-AUC
- Confusion Matrix
- Feature Importance

## 📊 Resultados Esperados

O projeto busca alcançar:
- **ROC-AUC > 0.80** para discriminação efetiva
- **Identificação clara** das top features mais impactantes
- **Insights acionáveis** para o departamento de RH

## 🔍 Principais Insights Típicos

Com base em análises similares, variáveis como:
- **BusinessTravel**: Viagens frequentes correlacionam com maior attrition
- **MonthlyIncome**: Salários mais baixos têm attrition maior
- **OverTime**: Funcionários com hora extra têm risco mais alto
- **WorkLifeBalance**: Insatisfação com equilíbrio impacta saída
- **YearsAtCompany**: Funcionários novos têm maior risco
- **Age & MaritalStatus**: Funcionários mais jovens e solteiros tendem a sair mais

## 📝 Autor

Trabalho desenvolvido como conclusão da disciplina **Machine Learning Aplicado**

## 📄 Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para detalhes.

## 📚 Recursos Úteis

- [IBM HR Analytics Dataset](https://www.kaggle.com/pavansubhasht/ibm-hr-analytics-attrition-dataset)
- [Scikit-learn Documentation](https://scikit-learn.org/)
- [Pandas Documentation](https://pandas.pydata.org/)

---

**Última atualização**: Junho de 2026
