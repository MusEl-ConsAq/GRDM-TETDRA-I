## **4. La Catena del Trasferimento Digitale**

### **4.1 L'architettura del sistema di digitalizzazione**

Il processo di trasferimento digitale dei nastri di Scelsi rappresenta un equilibrio delicato tra fedeltà filologica e praticabilità tecnica. Durante le sessioni di laboratorio, ho potuto osservare e partecipare direttamente all'implementazione di una catena di digitalizzazione che, pur basandosi su standard professionali consolidati, presenta specificità dettate dalla natura peculiare del materiale trattato.

Il cuore del sistema è costituito da un magnetofono Studer A800, macchina di riferimento nell'ambito del restauro audio professionale[^51].

La decisione di operare a 96 kHz di frequenza di campionamento e 24 bit di risoluzione rappresenta uno standard elevato ma non estremo nel campo del restauro audio[^52]. Durante le discussioni tecniche in laboratorio, Bernardini ha spiegato la logica di questa scelta:

1. **96 kHz di frequenza di campionamento**: garantisce una banda passante fino a 48 kHz, ben oltre il limite dell'udibile umano ma essenziale per catturare tutti gli artefatti e i rumori ad alta frequenza che possono fornire informazioni sulla datazione e identificazione dei nastri.

2. **24 bit di risoluzione**: offre un range dinamico teorico di 144 dB, ampiamente sufficiente per catturare sia il segnale utile che il rumore di fondo senza saturazione o perdita di dettaglio nei passaggi più deboli.

L'importanza di questi parametri diventa evidente considerando che "proprio quando i nastri sono di minore qualità e quindi hanno la maggiore quantità di rumore, è importante fissare con precisione il rumore, tutto il rumore possibile, perché questo rumore è indicativo"[^53]. Il rumore, in questo contesto, non è un elemento da eliminare ma informazione da preservare.

### **4.3 L'interfaccia Pro Tools: gestione e organizzazione**

Il segnale analogico proveniente dal magnetofono Studer A800 viene convertito in digitale attraverso un'interfaccia Digidesign 192 I/O, che rappresentava al momento dell'inizio del progetto lo standard di riferimento per le produzioni audio professionali[^54]. Questa interfaccia garantisce conversione AD/DA di alta qualità con jitter estremamente basso e stabilità di clock eccellente.

L'organizzazione delle sessioni Pro Tools segue un protocollo rigoroso sviluppato nel corso degli anni di lavoro:

1. **Tracce di trasferimento grezzo**: le prime tracce contengono il trasferimento continuo del nastro a diverse velocità, quando necessario. Questo approccio permette di preservare l'integrità del trasferimento originale prima di qualsiasi intervento di editing.

2. **Tracce di layout**: due tracce mono documentano la disposizione fisica del materiale sul nastro, essenziale per comprendere la struttura delle registrazioni bidirezionali.

3. **Tracce di riproduzione**: una (mono) o due (stereo) tracce contenenti la sequenza audio completa nell'ordine identificato come corretto, con tutte le velocità di lettura appropriate applicate[^55].

### **4.4 La gestione delle configurazioni non standard**

Un aspetto particolarmente complesso del processo riguarda la gestione dei nastri con configurazioni non standard. Durante il laboratorio ho potuto osservare diversi casi problematici:

**Nastri con velocità multiple**: alcuni nastri presentano sezioni registrate a velocità diverse all'interno della stessa bobina. La procedura prevede trasferimenti multipli dell'intero nastro a tutte le velocità possibili (9,5 cm/s, 19 cm/s, 38 cm/s), con successiva ricostruzione in post-produzione della sequenza corretta[^56].

**Registrazioni bidirezionali**: Le modalità di registrazione variano significativamente da nastro a nastro. Le registrazioni professionali utilizzano generalmente configurazione stereo, con le due piste che procedono nello stesso verso. I nastri domestici di Scelsi presentano invece spesso configurazione mono bidirezionale, con una pista che va al dritto e l'altra al rovescio. Durante la post-produzione è quindi necessario rovesciare la seconda pista per ascoltare tutto il contenuto in sequenza.

Alcuni nastri presentano registrazioni multiple in cui Scelsi passava da una pista all'altra riportando il segnale in feedback in varie direzioni. In questi casi, come osservato durante il laboratorio, "non si capisce veramente niente" e si deve assumere che il primo segnale sia quello della direzione giusta, mentre gli altri sono aggiunti successivamente[^57].

### **4.5 Le eccezioni al protocollo standard**

Nel corso del progetto sono emerse situazioni che hanno richiesto deviazioni dal protocollo standard. I nastri eccezionalmente lunghi, quando digitalizzati a 96 kHz, generano file che eccedono i limiti del file system HFS+ utilizzato dai computer Mac. In questi casi specifici, documentati nel database, si è optato per una frequenza di campionamento di 48 kHz[^58]. Questa decisione, presa per soli 3-4 nastri su oltre 300, rappresenta un compromesso accettabile considerando che si tratta generalmente di registrazioni di conferenze o materiale parlato dove l'estensione in frequenza è meno critica.

Un'altra eccezione riguarda i nastri gravemente danneggiati che possono essere riprodotti una sola volta. In questi casi, contrariamente al protocollo che prevede il passaggio preliminare per la misurazione, si procede direttamente al trasferimento digitale alla velocità stimata più probabile, accettando il rischio di una lettura non ottimale piuttosto che perdere completamente il contenuto.

### **4.6 Il flusso di lavoro post-trasferimento**

Una volta completato il trasferimento digitale, inizia la fase di post-produzione che, nel caso dei nastri di Scelsi, non prevede alcun intervento di restauro o pulizia del segnale. Questa scelta, apparentemente controintuitiva nel campo del restauro audio, riflette la filosofia del progetto: preservare l'integrità documentale delle registrazioni[^59].

La post-produzione si concentra invece sull'identificazione e catalogazione dei contenuti:

1. **Segmentazione in regioni**: identificazione di tutti i punti di start/stop del registratore, che delimitano le unità minime di registrazione continua.

2. **Numerazione progressiva**: assegnazione di identificatori univoci a ciascuna regione per facilitare il riferimento incrociato con il database.

3. **Annotazione testuale**: trascrizione di tutte le informazioni udibili (annunci vocali, commenti) e descrizione del contenuto musicale.

4. **Generazione di metadata**: compilazione di tutti i dati tecnici e descrittivi in formato strutturato per l'inserimento nel database.

### **4.7 Standard di archiviazione e formati**

La scelta dei formati di archiviazione riflette l'impegno verso standard aperti e duraturi. I file audio vengono salvati in formato AIFF (Audio Interchange File Format) con ordinamento dei byte big-endian, garantendo la massima compatibilità e longevità[^60]. Le sessioni Pro Tools, pur essendo in formato proprietario, vengono esportate anche in formato testo (ASCII) per preservare le informazioni di editing indipendentemente dal software specifico.

Il sistema di archiviazione prevede il salvataggio dei file digitali su un array di dischi Firewire 800 in configurazione RAID-1, più un disco aggiuntivo per il backup corrente. Al termine di ogni sessione viene eseguito un backup su disco[^61].

### **4.8 Documentazione fotografica e visiva**

La documentazione fotografica costituisce una componente essenziale del processo di archiviazione. Durante il trasferimento, vengono fotografate e scannerizzate sistematicamente tutte le scatole, i contenitori e le scritte presenti su di essi, inclusi eventuali fogli inseriti all'interno[^62]. Particolare attenzione viene dedicata alla documentazione delle giunture esistenti e delle corruzioni fisiche del nastro, con registrazione precisa della loro posizione lungo il supporto[^63]. 

Le sessioni Pro Tools vengono documentate attraverso snapshot salvati in formato TIFF, garantendo una registrazione visiva dell'organizzazione delle tracce e delle regioni identificate[^64]. Questa documentazione fotografica completa permette future verifiche e analisi senza necessità di manipolare nuovamente i nastri originali, contribuendo alla loro preservazione fisica.


[^51]: Trascrizione 002, specifica del magnetofono utilizzato.

[^52]: Bernardini, N., 'Recovering Giacinto Scelsi's Tapes', cit., p. 172.

[^53]: Trascrizione 002, importanza della cattura del rumore.

[^54]: Trascrizione 002, catena di trasferimento Pro Tools.

[^55]: Bernardini, N., 'Recovering Giacinto Scelsi's Tapes', cit., p. 173.

[^56]: Trascrizione 002, gestione velocità multiple.

[^57]: Trascrizione 003, problematiche di interpretazione.

[^58]: Trascrizione 002, eccezioni per file troppo grandi.

[^59]: Bernardini, N., Pellegrini, A.C., 'The Multimedia Archive', cit., p. 188.

[^60]: Bernardini, N., 'Recovering Giacinto Scelsi's Tapes', cit., p. 174.

[^61]: Bernardini, N., 'Recovering Giacinto Scelsi's Tapes', cit., p. 172; Trascrizione 002, procedura di backup.

[^62]: Trascrizione 002, documentazione fotografica di scatole e scritte.
[^63]: Bernardini, N., 'Recovering Giacinto Scelsi's Tapes', cit., p. 172.
[^64]: Ibid., p. 174.
