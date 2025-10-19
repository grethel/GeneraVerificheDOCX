GeneraVerificheDOCX è un generatore automatico di compiti in formato .docx pensato per docenti.
Il software consente di estrarre in modo casuale o manuale un insieme di domande da un paniere Excel, suddiviso per tipologia (risposta multipla o aperta), e di creare automaticamente più versioni personalizzate dei compiti.

Ogni compito viene salvato in una cartella dedicata, completo di punteggi, titoli e formattazione, pronto per la stampa o la distribuzione digitale.

✨ Funzionalità principali

Selezione del file Excel contenente le domande

Generazione casuale o manuale dei compiti

Mescolamento automatico delle domande e delle risposte

Creazione automatica di file Word (.docx) pronti all’uso

Gestione ordinata dei compiti generati in cartelle datate

⚙️ Tecnologie utilizzate

Python 3

pandas per la gestione dei dati

python-docx per la generazione dei documenti Word

os e datetime per la gestione dei file e delle cartelle

📂 Struttura delle cartelle

📁 domande/              → contiene i file Excel con le domande
📁 domande_manuali/      → contiene eventuali configurazioni manuali
📁 compiti/              → cartella di output dei compiti generati
📝 compitogen.py         → script principale

