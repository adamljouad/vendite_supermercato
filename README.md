# Superstore Sales Analysis

Analisi esplorativa di un dataset retail (Superstore) con focus sulla redditività delle categorie di prodotto.  
L'obiettivo è individuare quali categorie generano margini bassi o perdite e analizzare i fattori che possono influenzare la performance, come sconti e differenze geografiche.

---

## Obiettivo del progetto

L'analisi cerca di rispondere a queste domande:

- Quali categorie e sotto-categorie generano più profitto?
- Dove si concentrano le principali perdite?
- Gli sconti hanno un impatto sulla redditività?
- Esistono combinazioni specifiche tra categoria e regione con performance negative?

---

## Dataset

**Superstore Sales Dataset**

- 9.994 ordini
- 21 colonne
- Informazioni su:
  - vendite
  - profitto
  - sconti
  - categorie e sotto-categorie
  - regioni
  - date degli ordini e spedizioni

Il dataset non presenta valori mancanti.

---

## Strumenti utilizzati

- **Python (pandas)** → pulizia dati, trasformazioni e analisi esplorativa
- **SQL (SQLite)** → query aggregate per il calcolo dei KPI
- **Jupyter Notebook (VS Code)** → sviluppo dell'analisi
- **Tableau** → creazione della dashboard finale

---

## Analisi svolta

Il progetto è stato sviluppato attraverso:

1. Pulizia e preparazione dei dati
2. Analisi delle vendite e del profitto
3. Calcolo del margine di profitto
4. Analisi per categoria e sotto-categoria
5. Studio dell'impatto degli sconti
6. Analisi geografica per regione
7. Creazione di una dashboard interattiva in Tableau

---

## Principali insight

- Il margine medio complessivo è circa **12%**, ma presenta una forte variabilità tra gli ordini.
- La categoria **Furniture** genera vendite simili a **Technology** e **Office Supplies**, ma con una redditività molto più bassa (**~2,5% di margine**).
- Le principali perdite di Furniture sono concentrate nelle sotto-categorie:
  - **Tables** → perdita netta di circa **17.700€**
  - **Bookcases** → perdita netta di circa **3.500€**

---

## Analisi finale: Furniture nella regione Central

L'analisi per **Regione × Categoria** ha permesso di individuare il principale fattore associato alla perdita.

La categoria **Furniture** risulta in perdita solamente nella regione **Central**, dove presenta uno sconto medio molto superiore rispetto alle altre regioni:

| Regione | Sales Furniture | Profit Furniture | Sconto medio |
|---|---:|---:|---:|
| Central | 163.797€ | -2.871€ | 29,7% |
| East | 208.291€ | 3.046€ | 15,4% |
| South | 117.299€ | 6.771€ | 12,2% |
| West | 252.613€ | 11.505€ | 13,1% |

Il risultato suggerisce che gli sconti elevati applicati su Furniture nella regione Central siano un possibile driver della perdita di redditività.

---

## Dashboard Tableau

La dashboard include:

- KPI principali:
  - Total Sales
  - Total Profit
  - Profit Margin
- Analisi della redditività per categoria
- Confronto regionale
- Trend temporale di vendite e profitto

---

## Possibili sviluppi futuri

- Budget vs Actual Analysis
- Forecasting delle vendite
- Analisi della redditività per cliente
- Studio più approfondito dell'impatto degli sconti

