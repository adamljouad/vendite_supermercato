# Superstore Sales Analysis

Analisi esplorativa delle vendite di un retailer USA (dataset Superstore), con focus su KPI di redditività per categoria di prodotto — vendite, profitto, margine e impatto degli sconti.

## Obiettivo del progetto

Individuare quali categorie e sotto-categorie di prodotto generano margini bassi o perdite, e capire in che misura gli sconti applicati ne sono la causa. L'analisi replica il tipo di lavoro tipico di un ruolo di controllo di gestione: dall'esplorazione dei dati grezzi fino a un insight azionabile per il business.

## Dataset

[Superstore Sales Dataset](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final) — 9.994 ordini, 21 colonne (vendite, profitto, sconto, categoria, regione, date di ordine/spedizione, ecc.), nessun valore mancante.

## Strumenti utilizzati

- **Python (pandas)** — pulizia dati, feature engineering (conversione date, calcolo margine)
- **SQL (SQLite)** — query aggregate per il calcolo dei KPI
- Jupyter Notebook (VS Code)

## Struttura del progetto
├── data/
│   ├── superstore_raw.csv     # dataset originale
│   └── superstore.db          # database SQLite generato dai
                                 dati puliti
├── analysis.ipynb             # notebook con l'intera analisi
└── README.md
## Come eseguirlo

```bash
python3 -m venv venv
source venv/bin/activate
pip install pandas jupyter
```
Apri `analysis.ipynb` in VS Code (o Jupyter) e esegui le celle in ordine.

## Principali insight

- Il margine di profitto medio complessivo è **~12%**, ma con alta variabilità (deviazione standard 0.47) — alcuni ordini generano perdite fino al -275% del valore venduto.
- A livello di categoria, **Furniture** vende quasi quanto Office Supplies e Technology (~740k€), ma genera un margine drasticamente inferiore (~2.5% contro ~17%).
- Scomponendo per sotto-categoria, il problema è isolato in **Tables** (perdita netta di ~17.700€) e **Bookcases** (perdita netta di ~3.500€), entrambe con sconto medio più alto (26% e 21%) rispetto a Chairs e Furnishings, che restano profittevoli.
- Lo sconto medio da solo non spiega interamente il gap di margine tra categorie — segnale che serve un'analisi più granulare (es. distribuzione dei singoli ordini) per capire l'impatto reale degli sconti estremi.

## Prossimi sviluppi

- Analisi temporale (vendite/profitto mensili, stagionalità)
- Confronto per regione geografica
- Dashboard riassuntiva (Power BI)