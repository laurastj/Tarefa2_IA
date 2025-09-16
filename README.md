# Atividade de IA - Classificação com Titanic

Resumo:
Repositório com a atividade de classificação (tarefa 2) usando o dataset Titanic. O objetivo foi comparar modelos e documentar pré-processamento e resultados.

---

## Estrutura do repositório
- `notebooks/tarefa2.ipynb` — notebook principal (Google Colab).
- `src/` — scripts Python (opcional).
- `data/titanic.csv` — dataset (ou link abaixo).
- `outputs/` — gráficos e arquivos exportados.
- `requirements.txt` — pacotes necessários.

---

## Dataset
- Fonte: https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv  
- Target: `Survived` (0 = não, 1 = sim)

---

## Pré-processamento aplicado
- Colunas usadas: `Pclass`, `Sex`, `Age`, `SibSp`, `Parch`, `Fare`, `Embarked`
- Nulos: imputação por mediana (numéricas) e moda (categóricas)
- Escala: `StandardScaler` nas numéricas
- Codificação: `OneHotEncoder(handle_unknown='ignore', sparse_output=False)`

---

## Modelos treinados
- Decision Tree
- K-Nearest Neighbors (KNN)
- Logistic Regression

Métricas reportadas: Acurácia, Matriz de Confusão, Precision, Recall e F1-score.

---

## Principais resultados
- (Copie e cole aqui os valores das métricas que saíram no seu notebook, ex. `Logistic Regression — acurácia: 0.79, F1: 0.75`)
- Inserir gráfico comparativo:
  ![Gráfico de acurácias](outputs/acc_comparison.png)

---

## Conclusões e recomendações
- Principais features: `Sex`, `Pclass`, `Age`
- Melhorias sugeridas: feature engineering (`FamilySize`), balanceamento de classes (SMOTE), tuning (GridSearchCV), testar RandomForest/XGBoost.

---

## ▶ Como rodar
1. Abrir `notebooks/tarefa2.ipynb` no Google Colab (File → Upload notebook) ou no Jupyter local.
2. Se local: criar virtualenv e instalar packages:
   ```bash
   python -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
