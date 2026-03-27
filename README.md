# UECU
**Autore:** Denis Karaje

## Legenda e Navigazione
1. [Descrizione e Visione](#descrizione-e-visione)
2. [Analisi di Mercato](#analisi-di-mercato)
3. [Specifiche Tecniche](#specifiche-tecniche)
4. [Analisi dei Requisiti](#analisi-dei-requisiti)
5. [Modellazione e Prototipazione](#modellazione-e-prototipazione)
6. [Business Strategy](#business-strategy)

---

## Descrizione e Visione
UECU è una soluzione composta da **dispositivo fisico + app mobile**, progettata per permettere all’utente di monitorare, leggere e gestire i dati elettronici del proprio veicolo in modo semplice e guidato tramite smartphone.

Il dispositivo si collega all’auto e comunica via **Bluetooth** con l’app. L’app si connette a un **server centrale** che gestisce veicoli, dati, aggiornamenti, storico operazioni e servizi digitali. L’utente può controllare lo stato del veicolo, visualizzare informazioni tecniche e ricevere notifiche o assistenza da tecnici autorizzati.

L’obiettivo del progetto è rendere la gestione elettronica del veicolo:
- accessibile
- trasparente
- sicura
- digitale e scalabile

> Controlla la tua auto in pochi minuti, direttamente dal telefono.

---

## Analisi di Mercato

### Problema
Molti automobilisti che vogliono controllare lo stato elettronico del proprio veicolo devono affrontare:
- costo elevato della manodopera
- scarsa trasparenza
- difficoltà nell’ottenere informazioni tecniche
- tempi di attesa lunghi
- nessuno storico digitale degli interventi
- strumenti troppo complessi

### Target
Il progetto si rivolge a:
- Appassionati di auto
- Officine ed elettrauti
- Utenti privati
- Piccoli centri assistenza
- Preparatori

### Competitors
- App OBD generiche
- Strumenti diagnostici professionali
- Officine tradizionali
- Servizi di diagnosi standalone

### Analisi Comparativa

| Caratteristica | UECU | Officina | App OBD | Strumento professionale |
|---|---|---|---|---|
| Facilità d’uso | Alta | Media | Media | Bassa |
| Storico digitale | Sì | No | Limitato | Dipende |
| Controllo smartphone | Sì | No | Sì | No |
| Aggiornamenti online | Sì | No | Limitato | Dipende |
| Supporto remoto | Sì | Limitato | No | Limitato |
| Scalabilità | Alta | Bassa | Media | Media |

---

## Specifiche Tecniche

### Architettura del Sistema
Il sistema è composto da:

1. **Dispositivo UECU**
   - Collegamento al veicolo
   - Comunicazione Bluetooth
   - Memoria interna
   - Firmware aggiornabile

2. **App Mobile**
   - Login utente
   - Collegamento dispositivo
   - Visualizzazione dati
   - Storico operazioni
   - Notifiche

3. **Backend Cloud**
   - Gestione utenti
   - Gestione veicoli
   - Gestione dispositivi
   - Database storico
   - Servizi e aggiornamenti

4. **Database**
   - Utenti
   - Veicoli
   - Dispositivi
   - Storico operazioni
   - Diagnosi
   - Notifiche

### Stack Tecnologico
- App: Kotlin / Flutter
- Backend: Node.js / Java Spring
- Database: PostgreSQL / MongoDB
- Autenticazione: JWT
- Comunicazione: Bluetooth + HTTPS
- Hosting: Cloud / VPS

---

## Analisi dei Requisiti

### Requisiti Funzionali
Il sistema deve permettere di:
- Registrazione utente
- Login utente
- Associazione dispositivo
- Collegamento Bluetooth
- Visualizzazione dati veicolo
- Storico operazioni
- Notifiche
- Gestione account
- Supporto tecnico remoto
- Aggiornamento firmware dispositivo
- Gestione veicoli
- Gestione dispositivi

### User Stories

| Attore | Azione | Obiettivo |
|---|---|---|
| Utente | Registrarsi | Accedere alla piattaforma |
| Utente | Effettuare login | Usare i servizi |
| Utente | Collegare dispositivo | Comunicare con auto |
| Utente | Visualizzare dati | Controllare stato veicolo |
| Utente | Vedere storico | Monitorare interventi |
| Utente | Ricevere notifiche | Essere avvisato |
| Tecnico | Accedere al sistema | Fornire assistenza |
| Admin | Gestire database | Controllare sistema |

### Requisiti Non Funzionali
- Interfaccia semplice
- Sistema veloce
- Sistema sicuro
- Sistema scalabile
- Compatibilità con più veicoli
- Affidabilità elevata

### Requisiti di Dominio
- Il dispositivo deve essere associato a un account
- Le operazioni devono essere tracciate
- I dati devono essere salvati
- Accesso protetto
- Comunicazioni sicure

---

## Modellazione e Prototipazione

### Attori del Sistema
- Utente
- Dispositivo UECU
- App Mobile
- Server
- Tecnico
- Amministratore

### Flusso Principale
1. Login utente
2. Collegamento dispositivo
3. Lettura dati veicolo
4. Invio dati al server
5. Visualizzazione dati su app
6. Salvataggio storico
7. Eventuale assistenza tecnica

---

## Business Strategy

### Value Proposition
UECU combina:
- Hardware
- App
- Cloud
- Servizi digitali

### Modello di Business
Possibili entrate:
- Vendita dispositivo
- Abbonamento mensile
- Servizi premium
- Supporto tecnico
- Partnership con officine

### Elevator Pitch
UECU è una piattaforma composta da dispositivo e app che permette di monitorare e gestire i dati elettronici del veicolo in modo semplice e digitale. L’utente può controllare la propria auto dal telefono, avere uno storico digitale e ricevere assistenza tecnica. Il progetto digitalizza il rapporto tra veicolo, utente e officina, rendendolo più semplice, veloce e moderno.


---

## Modellazione e Prototipazione

### Use Case UML

```mermaid
flowchart LR
    U[Utente]
    D[Dispositivo UECU]
    A[App Mobile]
    S[Server Centrale]
    T[Tecnico]
    M[Amministratore]

    U --> UC1[Registrarsi]
    U --> UC2[Effettuare login]
    U --> UC3[Associare dispositivo]
    U --> UC4[Collegare il veicolo]
    U --> UC5[Visualizzare dati veicolo]
    U --> UC6[Consultare storico operazioni]
    U --> UC7[Ricevere notifiche]
    U --> UC8[Inviare richiesta assistenza]

    D --> UC9[Trasmettere dati all'app]
    D --> UC10[Sincronizzarsi con app]

    A --> UC11[Mostrare stato del veicolo]
    A --> UC12[Inviare dati al server]
    A --> UC13[Gestire notifiche e storico]

    T --> UC14[Analizzare richiesta tecnica]
    T --> UC15[Fornire supporto remoto]

    M --> UC16[Gestire utenti]
    M --> UC17[Gestire dispositivi]
    M --> UC18[Gestire database]
    M --> UC19[Pubblicare aggiornamenti]

    UC3 --> A
    UC4 --> D
    UC5 --> A
    UC6 --> A
    UC7 --> A
    UC8 --> S
    UC9 --> A
    UC12 --> S
    UC14 --> S
    UC16 --> S
