# Generatore di Verifiche Personalizzate

Un tool standalone per creare compiti e verifiche in formato Word (.docx) a partire da un file Excel di domande.  
 
---

## 📝 Funzionalità principali

- Generazione di compiti **casuale** o **manuale**.
- Supporto per **domande a risposta multipla (RM)** e **risposta aperta (RA)**.
- Possibilità di personalizzare:
  - **Intestazione**: “VERIFICA DI [MATERIA]” con riga Nome/Cognome/Classe/Data sulla prima pagina.
  - **Font e dimensione del testo**.
  - **Margini** superiori, inferiori, sinistro e destro.
  - **Layout a una o due colonne** per il corpo del testo.
- Domande a risposta aperta senza righe vuote aggiuntive.
- Creazione automatica di cartelle di output con timestamp.

---

## ⚡ Requisiti

- Windows 10/11 (64-bit consigliato)
- File Excel con le domande organizzate in colonne:
  - `Tipo` (RM o RA)
  - `Domanda`
  - `Risposta 1` … `Risposta 4` (per domande RM)

---

## 🚀 Utilizzo

1. Scaricare o copiare il file `GeneratoreCompiti.exe`.
2. Preparare la cartella `domande/` con i file Excel delle domande.
3. Avviare l’eseguibile facendo doppio clic su `GeneratoreCompiti.exe`.
4. Seguire le istruzioni interattive:
   - Inserire il nome della materia.
   - Scegliere margini, font, dimensione del carattere.
   - Decidere se usare due colonne o meno.
   - Selezionare modalità casuale o manuale.
   - Indicare numero di domande per tipo e punti assegnati.
5. I compiti generati saranno salvati nella cartella `compiti/` con timestamp.

---

 # Generatore di Verifiche Personalizzate

Un tool standalone per creare compiti e verifiche in formato Word (.docx) a partire da un file Excel di domande.  
Il programma è già compilato in formato `.exe` per Windows, quindi non è necessario installare Python.

---

## 📝 Funzionalità principali

- Generazione di compiti **casuale** o **manuale**.
- Supporto per **domande a risposta multipla (RM)** e **risposta aperta (RA)**.
- Possibilità di personalizzare:
  - **Intestazione**: “VERIFICA DI [MATERIA]” con riga Nome/Cognome/Classe/Data sulla prima pagina.
  - **Font e dimensione del testo**.
  - **Margini** superiori, inferiori, sinistro e destro.
  - **Layout a una o due colonne** per il corpo del testo.
- Domande a risposta aperta senza righe vuote aggiuntive.
- Creazione automatica di cartelle di output con timestamp.

---

## ⚡ Requisiti

- Windows 10/11 (64-bit consigliato)
- File Excel con le domande organizzate in colonne:
  - `Tipo` (RM o RA)
  - `Domanda`
  - `Risposta 1` … `Risposta 4` (per domande RM)

---

## 🚀 Utilizzo

1. Scaricare o copiare il file `GeneratoreCompiti.exe`.
2. Preparare la cartella `domande/` con i file Excel delle domande.
3. Avviare l’eseguibile facendo doppio clic su `GeneratoreCompiti.exe`.
4. Seguire le istruzioni interattive:
   - Inserire il nome della materia.
   - Scegliere margini, font, dimensione del carattere.
   - Decidere se usare due colonne o meno.
   - Selezionare modalità casuale o manuale.
   - Indicare numero di domande per tipo e punti assegnati.
5. I compiti generati saranno salvati nella cartella `compiti/` con timestamp.

---

## 📂 Struttura dei file

├── domande/
│ └── esempio_domande.xlsx
├── domande_manuali/
│ └── domande_manuali.xlsx
├── GeneratoreCompiti.exe
└── README.md

## 📌 Note

- L’intestazione è **solo sulla prima pagina** e rimane fuori dalle colonne.
- Le domande a risposta aperta non contengono righe vuote extra per migliorare la compattezza.
- Ogni documento Word generato rispetta i margini e il layout impostati.
- Nessuna installazione di Python richiesta: il programma è pronto all’uso.

---

## ✨ Autore

- **Lucia Intelisano**  
- GitHub:  https://github.com/grethel

