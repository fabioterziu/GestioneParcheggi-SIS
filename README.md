# 🚗 Parcheggio automatizzato con architettura FSMD (tool SIS)


## DESCRIZIONE:
Il progetto consiste nella gestione di un parcheggio automatizzato per automobili.  
Il parcheggio è suddiviso in tre settori:
- Settore “A” 31 posti disponibili massimi;  
- Settore “B” 31 posti disponibili massimi;  
- Settore “C” 24 posti disponibili massimi;
  
Al momento d’ingresso l’utente deve dichiarare in quale settore desidera parcheggiare.  
Analogamente al momento dell’uscita deve dichiarare da quale settore proviene.  
Il parcheggio rimane libero durante la notte, permettendo a tutte le macchine di entrare ed uscire a piacimento.  
La mattina il dispositivo viene acceso da un operatore tramite l’inserimento del codice a 5 bit ‘11111’.  
Al ciclo successivo il sistema attende l’inserimento del numero di automobili presenti nel settore “A”, memorizzandone il valore.  
Nei due cicli successivi avviene lo stesso per i settori “B” e “C”.  
Se dovesse venir inserito un valore superiore a quello del massimo numero di posti consentiti, il parcheggio verrà considerato pieno.  
A questo punto, ricevuti i valori d’ingresso che indicano quanti e quali posti macchina sono occupati, il sistema inizia il suo funzionamento autonomo, quindi ogni volta un utente si
dovrà avvicinare alla posizione di ingresso o uscita e premere un pulsante relativo al settore in cui intende parcheggiare oppure ha già parcheggiato.  
Il dispositivo si spegne quando riceve in input la sequenza ‘00000’.  

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
