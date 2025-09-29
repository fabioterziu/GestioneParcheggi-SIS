# 🚗 Parcheggio automatizzato CLI con Architettura FSMD (sintesi logica SIS)


## BREVE DESCRIZIONE:
Elaborato sviluppato in coppia per l'esame di Architettura degli Elaboratori (laboratorio) [Anno 2023].  

Il progetto consiste nella gestione di un parcheggio automatizzato per automobili.  
Al momento d’ingresso l’utente deve dichiarare in quale settore desidera parcheggiare.  
Analogamente al momento dell’uscita deve dichiarare da quale settore proviene.  
Il parcheggio rimane libero durante la notte, permettendo a tutte le macchine di entrare ed
uscire a piacimento.

## FLUSSO DI PROGETTAZIONE:
Il sistema è stato realizzato seguendo l'architettura FSMD (Macchina a Stati Finiti e Datapath).  
Questa metodologia distingue l'unità di controllo (FSM) dall'unità di elaborazione dati (DATAPATH).

- FSM:  
  KISS-> descrizione delle transizioni di stato

- DATAPATH:  
  BLIF-> descrizione strutturale per la creazione dei componenti, l'interconnessione, e la logica combinatoria.

SIS: strumento per la sintetizzazione e ottimizzazione di circuiti sequenziali  
-> sono stati minimizzazti e codificati gli stati FSM  
-> ottimizzato e mappato (per area e ritardo) il circuito finale FSMD



## NOTE

**(Per un'illustrazione più dettagliata consultare [“Relazione.pdf”](Relazione.pdf))**  

**REQUISITI E COMPATIBILITÀ:**  
Per eseguire il programma è necessario il tool SIS in ambiente UNIX/Linux  

**PER ESEGUIRE:**  
Avviare SIS nel terminale:  
sis

esegui:  
read_blif FSMD.blif  

statistiche:  
print_stats
