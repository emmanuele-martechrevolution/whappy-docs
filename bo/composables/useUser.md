# Documentazione Composable useUser

Il composable `useUser` gestisce le operazioni relative ai dati dell'utente, inclusa la richiesta e il reset delle informazioni.

## Definizione del Composable

**Posizione:** `src/composables/useUser.js`

### Funzioni

- **loadUser():**

  - **Descrizione:** Richiede i dati dell'utente attraverso il User Store.
  - **Processo:** Chiama il metodo `fetchUser` del User Store per ottenere i dati dell'utente.

- **clearUser():**
  - **Descrizione:** Resetta i dati dell'utente e lo stato attraverso il User Store.
  - **Processo:** Chiama il metodo `resetUser` del User Store per resettare i dati.

### Stato

- **user:** Dati dell'utente memorizzati nello User Store.
- **status:** Stato dell'operazione di richiesta dei dati dell'utente.
- **userLoaded:** Indica se i dati dell'utente sono stati caricati.

### Utilizzo

Per utilizzare `useUser`:

```javascript
import { useUser } from "@/composables/useUser";

const { loadUser, clearUser, user, status, userLoaded } = useUser();

// Esempio di richiesta dei dati dell'utente
await loadUser();
console.log(user); // Dati dell'utente

// Esempio di reset dei dati dell'utente
clearUser();
```
