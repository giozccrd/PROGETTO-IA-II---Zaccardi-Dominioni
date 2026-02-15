# Analisi della Progressione dell'HIV (Dataset ACTG 175)
## Progetto di Intelligenza Artificiale II - A.A. 2025/26

Questo progetto mira a sviluppare un modello di classificazione capace di predire la progressione della malattia (variabile target `cid`) in pazienti affetti da HIV, basandosi su dati clinici provenienti dallo studio randomizzato **ACTG 175**.

### Descrizione del Dataset
Il dataset contiene i dati di **2139 pazienti** e include diverse variabili demografiche e cliniche, tra cui:
* **Caratteristiche fisiche:** Età, peso (wtkg).
* **Parametri immunologici:** Conteggio iniziale di CD4 e CD8.
* **Storia clinica:** Trattamenti antiretrovirali precedenti e giorni di terapia.
* **Target (`cid`):** Variabile binaria (1 se vi è stata progressione della malattia, 0 altrimenti).

### Librerie Utilizzate
Il progetto è stato sviluppato in **Python 3** utilizzando le seguenti librerie:
* `ucimlrepo`: Per l'importazione diretta dei dati dal repository UCI.
* `pandas`: Per la manipolazione e pulizia dei dati.
* `seaborn` & `matplotlib`: Per l'analisi esplorativa (EDA) e la visualizzazione dei residui.
* `scikit-learn`: Per il preprocessing (StandardScaler), lo splitting dei dati e l'addestramento di modelli (Logistic Regression, k-NN, Random Forest).
* `xgboost`: Per l'implementazione del modello avanzato di Gradient Boosting.

### Struttura del Notebook
Il codice è organizzato nelle seguenti fasi:
1. **Importazione e Pulizia:** Caricamento dati e gestione dei valori mancanti.
2. **EDA:** Visualizzazione della distribuzione delle classi e mappe di correlazione.
3. **Preprocessing:** Feature Selection e standardizzazione tramite Z-score.
4. **Modellazione:** Confronto tra Logistic Regression, k-NN, Random Forest (ottimizzata con GridSearch) e XGBoost.
5. **Valutazione:** Analisi delle performance tramite residui probabilistici.

### Come eseguire il codice
Per riprodurre i risultati dell'analisi, segui questi passaggi:

1. **Google Colab (Consigliato):**
   * Carica il file `.ipynb` su [Google Colab](https://colab.research.google.com/).
   * Assicurati di installare la libreria UCI tramite il comando: `!pip install ucimlrepo`.
   * Esegui le celle in ordine cronologico.

2. **Esecuzione Locale:**
   * Clona la repository: `git clone <link-tua-repo>`.
   * Installa le dipendenze: `pip install pandas matplotlib seaborn scikit-learn xgboost ucimlrepo`.
   * Avvia Jupyter Notebook e apri il file del progetto.
