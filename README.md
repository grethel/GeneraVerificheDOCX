# Generatore di Verifiche Personalizzate

Questo progetto è un **generatore automatico di verifiche in formato Word (.docx)**, pensato per docenti che vogliono creare rapidamente compiti con domande a risposta multipla (RM) e a risposta aperta (RA).  

Il programma è distribuito come **file eseguibile Windows (.exe)**, quindi non richiede Python installato per l’uso finale.

---

## 📂 Struttura del progetto


- `domande/` → Contiene i file con le domande (RM e RA).  
- `domande_manuali/` → Contiene il file `domande_manuali.xlsx` che definisce quali domande includere nei compiti manuali.  
- `compiti/` → Cartella di output: ogni generazione crea una sottocartella timestamp con i compiti e una sottocartella `compiti_con_soluzione` con le copie per il docente.

---

## ⚡ Caratteristiche principali

- Supporta file **Excel (.xlsx) e CSV (.csv)**.  
- Non richiede intestazioni specifiche; legge le colonne in base alla posizione:
  - Colonna 1 → Tipo (`RM` o `RA`)  
  - Colonna 2 → Testo della domanda  
  - Colonne 3-6 → Risposte (solo per RM)  
- Generazione **casuale** o **manuale** dei compiti.  
- Creazione automatica della **copia con le risposte corrette** (risposte evidenziate con ✅).  
- Impostazione di margini, font (da elenco) e numero di colonne nel documento Word.  
- Punteggio personalizzabile per RM e RA.

---

## 🚀 Utilizzo

1. Posiziona i file delle domande nella cartella `domande/`.  
2. (Opzionale) Crea `domande_manuali/domande_manuali.xlsx` per la generazione manuale.  
3. Avvia l’eseguibile:


4. Segui le istruzioni a schermo:
   - Inserisci materia, margini, font e dimensione del carattere.  
   - Scegli modalità di generazione: casuale o manuale.  
   - Imposta numero di domande RM e RA, punti e numero di compiti.  

5. Troverai i compiti generati nella cartella `compiti/compiti_<timestamp>/` e le copie con soluzioni in `compiti_con_soluzione/`.

---

## 📝 Esempio di output

## 📝 Esempio di output

compiti/
└── compiti_20251024_203012/
├── compito_1.docx
├── compito_2.docx
└── compiti_con_soluzione/
├── compito_1_soluzioni.docx
└── compito_2_soluzioni.docx

## 💡 Note

- La risposta corretta per le domande RM è considerata sempre **la prima colonna di risposta** (`Risposta 1`) nel file originale.  
- Le domande RA non hanno risposte nel file, ma lo spazio per scriverle viene lasciato nel documento.  
- Il font può essere scelto da un elenco predefinito per evitare errori di digitazione.  
- Il programma è un `.exe` generato da uno script Python; l’utente finale **non necessita di Python**.

---

## 🧑‍💻 Autore

Creato da Lucia Intelisano – Generatore di verifiche personalizzate in formato Word.
