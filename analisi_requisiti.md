
# Documento di Analisi dei Requisiti

## Titolo del progetto
**SpaceRaiders – Web Game Multiplayer a Tema Navicelle Spaziali**

## 1. Introduzione

### 1.1 Scopo del progetto
Lo scopo del progetto è la realizzazione di un'applicazione web multiplayer che consenta a più utenti di partecipare a partite ambientate nello spazio, controllando navicelle dotate di funzionalità avanzate, potenziamenti, e interagendo con un sistema dinamico di eventi casuali e boss finali. Il progetto punta a valorizzare la fase di progettazione e l'uso di tecnologie moderne su architettura RESTful.

### 1.2 Tecnologie utilizzate
- **Frontend**: HTML5, CSS3, JavaScript (architettura MVP)
- **Backend**: PHP (API RESTful)
- **Containerizzazione**: Docker (obbligatoria lato server, facoltativa lato client)
- **Persistenza dati**: Database relazionale (es. MySQL)
- **Testing**: Unit test (PHPUnit), test di integrazione REST

## 2. Requisiti

### 2.1 Requisiti funzionali (RF)
| Codice | Requisito | Descrizione |
|--------|-----------|-------------|
| RF1 | Registrazione/Login utente | L’utente può creare un account e autenticarsi. |
| RF2 | Creazione/partecipazione partite | L’utente può creare una nuova partita o partecipare a una esistente. |
| RF3 | Invito amici | È possibile invitare altri giocatori a una partita. |
| RF4 | Gestione navicelle | Ogni navicella è controllata da almeno 2 giocatori. |
| RF5 | Potenziamenti | I giocatori raccolgono oggetti che migliorano le prestazioni della navicella. |
| RF6 | Eventi casuali | Durante le partite si attivano eventi casuali che influenzano il gameplay. |
| RF7 | Boss finale | Ogni mappa ha un boss da sconfiggere al termine. |
| RF8 | Progresso e difficoltà dinamica | La difficoltà si adatta in base a progressi e numero di giocatori. |
| RF9 | Punti e upgrade | I giocatori guadagnano punti per potenziare le navicelle tra una partita e l’altra. |
| RF10 | Selezione mappa | Le partite possono svolgersi su una delle 10 mappe predefinite. |
| RF11 | Creazione manuale mappe | L’utente può creare nuove mappe e caricarle sul server per altri utenti. |
| RF12 | Tabella record | Visualizzazione dei migliori punteggi e partite. |

### 2.2 Requisiti non funzionali (RNF)
| Codice | Requisito | Descrizione |
|--------|-----------|-------------|
| RNF1 | Architettura REST | Comunicazione esclusivamente tramite API REST CRUD |
| RNF2 | MVP | Struttura client in architettura Model-View-Presenter |
| RNF3 | Docker Server | Il backend deve essere eseguibile in un container Docker |
| RNF4 | Scalabilità | Supporto al gioco tra più utenti su dispositivi distinti |
| RNF5 | Personalizzazione estetica* | Skin sbloccabili completando mappe (da confermare) |
| RNF6 | Potenziamenti combinati* | Meccanica avanzata di potenziamento con combinazioni (da confermare) |

### 2.3 Requisiti premiali
| Codice | Requisito | Descrizione |
|--------|-----------|-------------|
| RP1 | Generazione mappe automatica | Creazione automatica di mappe con elementi casuali |
| RP2 | Docker lato client | Simulazione di client su più dispositivi |
| RP3 | Gioco online | I client devono essere connessi da dispositivi separati |
| RP4 | Configurazione controlli | Personalizzazione dei comandi da tastiera/controller |

## 3. Attori del sistema

| Attore | Descrizione |
|--------|-------------|
| Utente | Giocatore registrato che partecipa alle partite |
| Admin (opzionale) | Gestisce mappe, partite, utenti |

## 4. Casi d’uso principali

- UC1: Registrazione e login
- UC2: Creazione di una nuova partita
- UC3: Partecipazione a partita tramite invito
- UC4: Selezione o creazione mappa
- UC5: Inizio partita e interazione con altri utenti
- UC6: Raccoglimento potenziamenti
- UC7: Attivazione di eventi casuali
- UC8: Sconfitta boss finale
- UC9: Visualizzazione classifica
- UC10: Upgrade della navicella

## 5. Vincoli

- L’applicazione deve rispettare l’architettura REST-full CRUD
- Lato server sviluppato in PHP e containerizzato via Docker
- Nessun tipo di comunicazione alternativa al REST è permesso
- Interfaccia client costruita con HTML5, CSS3, JavaScript
- Utilizzo di architettura MVP lato frontend

## 6. Priorità

- Tutti i **requisiti minimi** sono **obbligatori**
- I requisiti **segnati come “DUBBIO”** saranno oggetto di validazione futura
- I requisiti **premiali** sono opzionali ma incentivati
