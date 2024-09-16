# Documentazione degli Store Pinia

In questo progetto utilizziamo Pinia come libreria di gestione dello stato per Vue 3. Questo documento fornisce una panoramica sugli store Pinia utilizzati nell'applicazione.

## Panoramica degli Store

Abbiamo i seguenti store Pinia:

1. **Auth Store** (`auth`)
2. **Config Store** (`config`)
3. **User Store** (`user`)

Ogni store è responsabile della gestione di specifiche parti dello stato dell'applicazione e fornisce le azioni e i getter necessari per la gestione dello stato.

---

### Auth Store

- **Posizione:** `src/stores/auth.js`
- **Scopo:** Gestisce lo stato di autenticazione, inclusa la gestione dei token e le funzionalità di login/logout dell'utente.

### Config Store

- **Posizione:** `src/stores/config.js`
- **Scopo:** Fornisce dettagli di configurazione come URL API basati sulla compagnia corrente.

### User Store

- **Posizione:** `src/stores/user.js`
- **Scopo:** Gestisce i dati dell'utente, inclusa la richiesta delle informazioni dell'utente dall'API e il reset dello stato dell'utente.

Per una documentazione dettagliata su ciascuno store, fare riferimento ai file di documentazione specifici.
