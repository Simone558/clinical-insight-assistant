State — 2026-06-07
Settimana corrente: 3 | Blocco: 1
Fatto

Cross-validation stratificata (StratifiedKFold, 5 fold) → AUC media 0.953, std 0.011 — modello stabile
Metriche avanzate: precision 0.797, recall 0.855, F1 0.825, PR-AUC 0.901
Grafico Precision-Recall Curve
Gestione classi sbilanciate: SMOTE (risultati quasi identici al baseline — dataset non troppo sbilanciato) + threshold tuning a 0.3 (recall +0.02, precision -0.03)
Calibrazione probabilità: CalibratedClassifierCV con isotonic regression + reliability diagram
SHAP: waterfall plot (analisi locale) + beeswarm plot (analisi globale)
Push notebook wk3_evaluation.ipynb su GitHub

Risultati
MetricaValoreCV AUC (media)0.953CV AUC (std)0.011Precision0.797Recall0.855F10.825PR-AUC0.901
Concetti chiari

Cross-validation stratificata: perché serve, come funziona, differenza con singolo train/test split
Precision vs recall: definizioni, trade-off, quando privilegiare l'una o l'altra in ambito clinico
PR-AUC: più informativa di ROC-AUC su classi sbilanciate
SMOTE: crea esempi sintetici della classe minoritaria, solo su training set
Threshold tuning: sposta la soglia di decisione senza ritrainare
Calibrazione: allinea le probabilità predette alla realtà — importante quando le probabilità vengono usate direttamente
SHAP waterfall: analisi locale, spiega una singola predizione
SHAP beeswarm: analisi globale, importanza delle feature su tutto il dataset
f(x) in SHAP è in log-odds, non in probabilità — va convertito con sigmoide

Concetti ancora confusi

Nessuno per ora

Domande aperte

Nessuna per ora

Prossimi step (Wk4)

PyTorch dalle basi: tensori, autograd, training loop manuale
MLP sui dati tabulari del Blocco 1 (confronto con XGBoost)
Concetti: backprop, loss function, optimizer, batch/epoch

Repo / file
https://github.com/Simone558/clinical-insight-assistant