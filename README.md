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


📋 Struttura del / dei file Excel delle domande

Perché il programma funzioni correttamente, i file Excel devono rispettare una struttura ben definita. Di seguito le indicazioni su come formattare i fogli di calcolo.

1. Foglio singolo e intestazioni obbligatorie

Il file Excel deve avere un solo foglio (o almeno le domande devono risiedere in un foglio principale)

Le colonne intestazione (header) devono essere presenti nella prima riga

I nomi delle colonne devono essere esatti (case sensitive in parte) come descritto qui sotto

2. Colonne richieste

Ecco le colonne richieste / supportate e il loro significato:

Colonna	Obbligatoria	Descrizione
Tipo	Sì	Deve essere “RM” per domande a Risposta Multipla oppure “RA” per domande a Risposta Aperta
Domanda	Sì	Il testo della domanda, che sarà stampato nel compito
Risposta 1, Risposta 2, Risposta 3, Risposta 4	Solo per RM	Le possibili opzioni, se la colonna esiste e il valore non è vuoto, viene considerata come opzione valida
(Altre colonne – opzionali)	No	Puoi aggiungere altre colonne (es. categoria, livello, tag, spiegazione) purché non interferiscano con le colonne obbligatorie

Nota bene:

Per le domande a risposta aperta (“RA”), non è necessario avere le colonne “Risposta 1…4”. Se presenti, verranno ignorate.

Se in una riga di “RM” alcune colonne tra “Risposta 1 … Risposta 4” sono vuote o non presenti, verranno semplicemente escluse dalla generazione delle opzioni.

3. Esempio di file Excel

Immagina un file chiamato domande_esempio.xlsx con questo contenuto:

Tipo	Domanda	Risposta 1	Risposta 2	Risposta 3	Risposta 4
RM	Qual è la capitale d’Italia?	Roma	Milano	Napoli	Torino
RM	Quale numero è primo?	4	9	7	10
RA	Spiega la teoria della relatività.				
RA	Quali sono le caratteristiche dell’acqua?				

Le prime due righe sono domande a risposta multipla (RM) e hanno quattro opzioni

Le ultime due sono a risposta aperta (RA) e non richiedono opzioni

4. File per generazione manuale

Se utilizzi la modalità manuale (genera_manuale), è richiesto un file di configurazione chiamato domande_manuali.xlsx nella cartella domande_manuali/. Le sue colonne tipiche possono essere:

Compito	RM	RA
1	“1,3,5”	“2,4”
2	“2,4,6”	“3,5”

Compito: numero identificativo del compito

RM: una stringa con gli indici (1-based) delle domande RM da includere

RA: una stringa con gli indici delle domande RA da includere

Questi indici devono riferirsi alle righe del file principale di domande (solo alle righe pertinenti di quel tipo, RM o RA). Il programma leggerà quelle righe, le mescolerà e genererà il compito corrispondente.

