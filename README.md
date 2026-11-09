# EcoPulse AI – Previsione fotovoltaica e gestione di uno storage
Progetto dimostrativo in due parti sulla non programmabilità del solare.
## 1. Logica dello storage
Una batteria da 400 kWh si carica quando il prezzo è basso e si scarica quando è alto (efficienza 90%). Su una giornata simulata: 128,7 € senza batteria, 151,9 € con batteria (+23,2 €, +18%). Prezzi e produzione sono inventati.
- Foglio di calcolo:https://docs.google.com/spreadsheets/d/1DH5_hsBXHzgyPlZAYbKxmqfo1MIOd8q5w5L6_pEylkw/edit?usp=sharing
- Notebook Python: [01_storage_logica.ipynb](01_storage_logica.ipynb)

## 2. Previsione con Machine Learning
Random Forest contro la baseline "domani = oggi" su un impianto ipotetico da 500 kWp, con dati meteo reali di Roma (2025). Errore medio orario nel test (fine ottobre–dicembre): baseline 9,2 kWh; modello 9,4 kWh; modello con altezza del sole 9,9 kWh. **Il modello non batte la baseline.**
- Notebook: [Ecopulse_livello_2.ipynb](Ecopulse_livello_2.ipynb)

## Limiti
- Produzione calcolata con una formula, non misurata
- Meteo osservato usato al posto delle previsioni
- Nuvolosità come stima grezza dell'irraggiamento
- Prezzi inventati

## Sviluppi futuri
Previsioni di irraggiamento archiviate, prezzi reali (GME), produzione reale (ENTSO-E / Terna).

## Strumenti e crediti
Python, pandas, scikit-learn, Google Colab, Google Fogli. Dati meteo: [Open-Meteo.com](https://open-meteo.com/). Sviluppato con l'IA come tutor.
