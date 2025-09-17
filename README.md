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
- == Decision Tree ==
Acurácia: 0.8044692737430168
              precision    recall  f1-score   support

           0       0.83      0.86      0.84       110
           1       0.77      0.71      0.74        69

    accuracy                           0.80       179
   macro avg       0.80      0.79      0.79       179
weighted avg       0.80      0.80      0.80       179

== KNN ==
Acurácia: 0.8212290502793296
              precision    recall  f1-score   support

           0       0.82      0.90      0.86       110
           1       0.81      0.70      0.75        69

    accuracy                           0.82       179
   macro avg       0.82      0.80      0.81       179
weighted avg       0.82      0.82      0.82       179

== Logistic Regression ==
Acurácia: 0.8044692737430168
              precision    recall  f1-score   support

           0       0.81      0.89      0.85       110
           1       0.79      0.67      0.72        69

    accuracy                           0.80       179
   macro avg       0.80      0.78      0.79       179
weighted avg       0.80      0.80      0.80       179

  ![Gráfico de acurácias](outputs/acc_comparison.png)

---

## Conclusões e recomendações
- Principais features: `Sex`, `Pclass`, `Age`
- Melhoria sugerida: feature engineering (FamilySize = SibSp + Parch + 1).

---

## ▶ Como rodar
1. Abrir `notebooks/tarefa2.ipynb` no Google Colab (File → Upload notebook) ou no Jupyter local.
