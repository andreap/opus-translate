# Opus Translation

Un progetto per la traduzione automatica di documenti Word dall'italiano all'inglese utilizzando il modello Helsinki-NLP.

## Requisiti

- Python 3.9 o superiore
- Conda (per la gestione dell'ambiente virtuale)
- Git

## Installazione

1. Clona il repository:
```bash
git clone https://github.com/yourusername/opus-translation.git
cd opus-translation
```

2. Crea e attiva l'ambiente conda (facoltativo):
```bash
conda create -n opus-translate python=3.9
conda activate opus-translate
```

3. Installa le dipendenze:
```bash
pip install -r requirements.txt
```

4. Installa huggingface-cli:
```bash
pip install huggingface_hub
```

5. Scarica il modello di traduzione:
```bash
huggingface-cli download Helsinki-NLP/opus-mt-it-en
```

## Struttura del Progetto

```
opus-translation/
├── it/                 # Cartella per i documenti in italiano
├── en/                 # Cartella per i documenti tradotti
├── models/            # Cartella per i modelli scaricati
├── model.ipynb         # Notebook principale con il codice di traduzione
├── requirements.txt    # Dipendenze del progetto
└── README.md          # Questo file
```

## Utilizzo

1. Assicurati che l'ambiente conda sia attivo:
```bash
conda activate opus-translate
```

2. Apri il notebook:
```bash
jupyter notebook model.ipynb
```

3. Posiziona i documenti Word da tradurre nella cartella `it/`

4. Esegui tutte le celle del notebook in sequenza

5. I documenti tradotti verranno salvati nella cartella `en/` con il suffisso "_EN"

## Configurazione

Il modello di traduzione può essere configurato modificando il dizionario `TRANSLATION_CONFIG` nel notebook. Le opzioni disponibili sono:

- `model_name`: Il modello di traduzione da utilizzare
- `framework`: Il framework di deep learning (pt per PyTorch)
- `device`: Il dispositivo su cui eseguire la traduzione (cpu o cuda)

## Note

- I file nella cartella `it/` e `en/` non vengono tracciati da Git
- Assicurati di avere sufficiente spazio su disco per i modelli di traduzione
- La prima esecuzione potrebbe richiedere più tempo per il download del modello
- Il modello scaricato localmente permette di lavorare offline e velocizza le esecuzioni successive

## Licenza

MIT License 