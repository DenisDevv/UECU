# **UECU**

**Autore:** Denis Karaje

## **Legenda e Navigazione**

1. **[Descrizione e Visione](#descrizione)**
2. **[Analisi di Mercato](#problema)** (Problema, Target, Competitors)
3. **[Specifiche Tecniche](#tecnologie)**
4. **[Analisi dei Requisiti](#analisi-dei-requisiti)** (Dettagli, Elenco e User Stories)
5. **[Modellazione e Prototipazione](#use-case-uml)** (UML e Prototipo)
6. **[Business Strategy](#elevator-pitch-e-business-model)** (Pitch, Business Model, WBS e Gantt)

---

## **Descrizione:**

UECU è una piattaforma composta da **dispositivo fisico + app mobile**, progettata per permettere agli utenti di **monitorare, leggere e gestire i dati elettronici del proprio veicolo** in modo semplice e guidato tramite smartphone.

Il dispositivo si collega al veicolo e comunica via **Bluetooth** con l’app. L’app si connette a un **server centrale** che gestisce veicoli, dati, aggiornamenti, storico operazioni e servizi digitali.

Un modo innovativo per gestire la propria auto: **meno costi, più controllo, più trasparenza**.

> ✨ *Controlla la tua auto in pochi minuti, direttamente dal telefono.*

---

## **Problema**

L’ostacolo principale identificato nel mercato attuale è il seguente:

> La difficoltà nell’accedere ai dati elettronici del proprio veicolo in modo semplice, economico e trasparente.

---

## **Target**

Il servizio si rivolge specificamente a:

- Appassionati di auto  
- Utenti privati  
- Officine ed elettrauti  
- Centri assistenza  
- Preparatori  

---

## **Competitors**

Il panorama attuale offre diverse alternative, ma nessuna integra **hardware + app + cloud + supporto remoto**:

* App OBD generiche  
* Officine tradizionali  
* Strumenti diagnostici professionali  

---

### **Analisi Comparativa**

| 🧩 **Caratteristica** | ⭐ **Importanza** | 🚗 **UECU** | 🔧 **Officina** | 📱 **App OBD** | 🛠️ **Strumenti Pro** |
|---|---|---|---|---|---|
| **Controllo da smartphone** | 🔥 High | 🟢 Completo | 🔴 No | 🟢 Sì | 🔴 No |
| **Storico digitale** | 🔥 High | 🟢 Completo | 🔴 No | 🟠 Limitato | 🟠 Dipende |
| **Supporto remoto** | 🔥 High | 🟢 Sì | 🔴 No | 🔴 No | 🟠 Limitato |
| **Facilità d’uso** | 🔥 High | 🟢 Alta | 🟠 Media | 🟠 Media | 🔴 Bassa |
| **Costo accessibile** | 🔥 High | 🟢 Medio/Basso | 🔴 Alto | 🟢 Basso | 🔴 Alto |
| **Aggiornamenti online** | 🔥 High | 🟢 Sì | 🔴 No | 🟠 Limitato | 🟠 Possibile |
| **Esperienza digitale completa** | 🔥 High | 🟢 Ecosistema | 🔴 No | 🟠 Parziale | 🟠 Tecnica |

---

## **Tagline**

> “La tua auto, i tuoi dati, il tuo controllo.”

---

## **Tecnologie**

Per supportare l’architettura del sistema:

* **App Mobile:** Kotlin / Flutter  
* **Backend:** Node.js (Express) o Java Spring  
* **Database:** PostgreSQL / MongoDB  
* **Autenticazione:** JWT  
* **Comunicazione:** Bluetooth + HTTPS  
* **Cloud:** VPS / AWS / Google Cloud  
* **Firmware:** aggiornabile OTA  
* **Sicurezza:** HTTPS, cifratura dati  

---

## **Analisi dei Requisiti**

### **Descrizione dei requisiti**

La piattaforma consente agli utenti di **registrarsi**, effettuare **login**, associare un dispositivo e collegarlo al veicolo.

L’utente può:

- visualizzare dati del veicolo  
- consultare lo storico  
- ricevere notifiche  
- richiedere assistenza  

Il sistema gestisce tutto tramite backend cloud e database.

---

### **Elenco Riassuntivo Requisiti**

#### **Funzionali**

* Registrazione e login  
* Associazione dispositivo  
* Collegamento Bluetooth  
* Lettura dati veicolo  
* Storico operazioni  
* Notifiche  
* Supporto tecnico remoto  
* Gestione dispositivi  
* Aggiornamento firmware  

---

### **User Story**

| **Attore (Come...)** | **Voglio...** | **In modo da...** |
|---|---|---|
| Utente | registrarmi | accedere al sistema |
| Utente | collegare dispositivo | leggere dati auto |
| Utente | vedere dati | controllare stato |
| Utente | vedere storico | monitorare interventi |
| Utente | ricevere notifiche | essere aggiornato |
| Tecnico | accedere ai dati | fornire supporto |
| Admin | gestire sistema | controllare tutto |

---

#### **Non Funzionali**

* Interfaccia semplice  
* Sistema veloce  
* Alta sicurezza  
* Scalabilità  
* Compatibilità multi-veicolo  

---

#### **Di Dominio**

* Dispositivo associato a utente  
* Dati tracciati e salvati  
* Comunicazioni protette  
* Accesso sicuro  

---

## **Use Case UML**

```mermaid
flowchart LR
    U[Utente]
    D[Dispositivo]
    A[App]
    S[Server]
    T[Tecnico]
    M[Admin]

    U --> Login
    U --> Associa
    U --> Visualizza
    U --> Storico
    U --> Notifiche

    D --> App
    A --> Server
    T --> Server
    M --> Server
```
---

## Prototipo

### Accesso diretto:

- https://uecu.lovable.app

---

## Elevator Pitch

 UECU è una piattaforma composta da dispositivo e app che permette di monitorare i dati del veicolo in modo semplice e digitale. L’utente può controllare la propria auto dal telefono, avere uno storico completo e ricevere assistenza tecnica. UECU rende il controllo del veicolo più moderno, veloce e accessibile.

---

WBS (Work Breakdown Structure)
```mermaid
graph LR
    A["UECU<br/>(4 mesi – €30k)"]

    A --> B["1. Progettazione<br/>(€4k – 3 sett.)"]
    B --> B1["Requisiti"]
    B --> B2["Architettura"]

    A --> C["2. Hardware<br/>(€7k – 5 sett.)"]
    C --> C1["Dispositivo"]
    C --> C2["Bluetooth"]
    C --> C3["Firmware"]

    A --> D["3. Backend<br/>(€8k – 6 sett.)"]
    D --> D1["Database"]
    D --> D2["API"]
    D --> D3["Servizi"]

    A --> E["4. App Mobile<br/>(€8k – 6 sett.)"]
    E --> E1["UI"]
    E --> E2["Connessione"]
    E --> E3["Dashboard"]

    A --> F["5. Testing<br/>(€3k – 3 sett.)"]
    F --> F1["Test"]
    F --> F2["Bugfix"]
```
---

## Cronoprogramma

```mermaid
gantt
    title UECU – Cronoprogramma (4 mesi)
    dateFormat  YYYY-MM-DD

    section Progettazione
    Analisi           :a1, 2026-01-01, 7d
    Architettura      :a2, after a1, 7d

    section Hardware
    Prototipo         :b1, 2026-01-15, 14d
    Bluetooth         :b2, after b1, 14d

    section Backend
    Database          :c1, 2026-02-01, 7d
    API               :c2, after c1, 14d

    section App
    UI                :d1, 2026-02-10, 14d
    Funzionalità      :d2, after d1, 14d

    section Testing
    Test              :e1, 2026-03-20, 7d
    Bugfix            :e2, after e1, 7d
    Beta              :milestone, 2026-04-01, 0d
```
