# State — 2026-06-04
Settimana corrente: 2 | Blocco: 1

## Fatto
- Preprocessing: imputation mediana globale, train/test split 80/20 con random_state=42, StandardScaler fit su x_train
- Trained 4 modelli: Logistic Regression, Decision Tree, Random Forest, Gradient Boosting
- Metriche calcolate: accuracy + ROC-AUC per tutti i modelli
- Push notebook `wk2_ml_baseline.ipynb` su GitHub

## Risultati
| Modello | Accuracy | ROC-AUC |
|---|---|---|
| Logistic Regression | 0.77 | 0.84 |
| Decision Tree | 0.82 | 0.82 |
| Random Forest | 0.88 | 0.93 |
| Gradient Boosting | 0.87 | 0.94 |

## Modello scelto
Gradient Boosting — ROC-AUC più alta (0.94), metrica più affidabile su classi sbilanciate. Interpretabile con SHAP in Wk3.

## Concetti chiari
- Differenza accuracy vs ROC-AUC e quando usare l'una o l'altra
- Logica predict vs predict_proba
- Perché fit dello scaler solo su x_train (data leakage)
- Intuizione dei 4 algoritmi e progressione LR → DT → RF → GB
- random_state per riproducibilità

## Concetti ancora confusi
- Sintassi pandas: ancora qualche incertezza

## Domande aperte
- Confrontare imputation mediana globale vs per gruppo in Wk3 — impatto sulle metriche?

## Prossimi step (Wk3)
- Cross-validation stratificata
- Metriche avanzate: precision/recall/F1, PR-AUC
- Gestione classi sbilanciate (SMOTE, class_weight, threshold tuning)
- Calibrazione probabilità
- SHAP per feature importance

## Repo / file
https://github.com/Simone558/clinical-insight-assistant