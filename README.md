# Predizione della progressione del diabete

Progetto di Machine Learning Advanced dedicato alla previsione della progressione del diabete dopo un anno attraverso un problema di regressione supervisionata.

## Obiettivo

L'obiettivo del progetto è sviluppare e valutare un modello capace di prevedere la progressione del diabete utilizzando il Diabetes dataset disponibile in Scikit-learn.

Il progetto è stato realizzato a scopo didattico e non è destinato all'utilizzo clinico o diagnostico.

## Dataset

Il dataset contiene:

- 442 osservazioni;
- 10 variabili;
- 1 variabile target;
- nessun valore mancante.

Il dataset è già standardizzato, quindi non è stato necessario applicare ulteriori tecniche di scaling.

## Tecnologie utilizzate

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Metodologia

Il progetto segue le principali fasi di un processo di Machine Learning:

1. caricamento e analisi del dataset;
2. analisi esplorativa dei dati;
3. studio delle correlazioni;
4. controllo dei valori mancanti e degli outlier;
5. suddivisione in training e test set;
6. creazione di una Linear Regression come baseline;
7. addestramento di un Random Forest Regressor;
8. ottimizzazione degli iperparametri con GridSearchCV;
9. valutazione e confronto delle prestazioni.

## Analisi esplorativa

Le variabili maggiormente associate al target sono risultate:

- BMI: correlazione pari a 0,59;
- S5: correlazione pari a 0,57;
- BP: correlazione pari a 0,44;
- S4: correlazione pari a 0,43.

Non sono stati individuati valori mancanti e gli outlier rilevati sono risultati limitati.

## Modello baseline

Come modello di riferimento è stata utilizzata una **Linear Regression**.

Risultato:

- R²: **0,453**

La baseline è stata utilizzata per verificare se un modello più complesso riuscisse a ottenere un miglioramento reale.

## Modello finale

Il modello finale selezionato è un **Random Forest Regressor**, ottimizzato tramite `GridSearchCV` con validazione incrociata a 5 fold.

Migliori iperparametri:

- `n_estimators = 200`
- `max_depth = 3`

### Prestazioni finali

| Metrica | Risultato |
|---|---:|
| R² | 0,476 |
| MAE | 42,714 |
| RMSE | 52,672 |

Il Random Forest Regressor ha ottenuto un risultato leggermente superiore rispetto alla Linear Regression, mostrando una migliore capacità di rappresentare alcune relazioni non lineari presenti nei dati.

## Confronto dei modelli

| Modello | R² |
|---|---:|
| Linear Regression | 0,453 |
| Random Forest Regressor | 0,476 |

Il miglioramento è contenuto, ma evidenzia il valore del confronto tra una baseline semplice e un modello più complesso.

## File presenti

- [`AngelicaButiML.ipynb`](AngelicaButiML.ipynb): notebook completo;
- [`Presentazione di AngelicaButiML.pdf`](Presentazione%20di%20AngelicaButiML.pdf): presentazione del progetto.

## Come eseguire il progetto

1. Scaricare o clonare la repository.
2. Installare le librerie necessarie: `pandas`, `numpy`, `matplotlib`, `seaborn` e `scikit-learn`.
3. Aprire `AngelicaButiML.ipynb` con Jupyter Notebook o JupyterLab.
4. Eseguire le celle in ordine.

Il dataset viene caricato direttamente attraverso Scikit-learn, quindi non è necessario scaricare file CSV esterni.

## Conclusioni

Il progetto ha mostrato l'intero processo di sviluppo di un modello di regressione:

- analisi esplorativa;
- valutazione del preprocessing;
- creazione di una baseline;
- ottimizzazione del modello;
- confronto delle prestazioni.

Il modello finale costituisce una buona base didattica, pur lasciando spazio a ulteriori miglioramenti.

## Autrice

**Angelica Buti**

Progetto realizzato durante il mio percorso formativo nell'ambito del Machine Learning Advanced.
