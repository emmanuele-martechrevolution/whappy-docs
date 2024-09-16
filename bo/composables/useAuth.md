# Documentazione Composable useAuth

Il composable `useAuth` gestisce le operazioni di autenticazione, inclusi il login e il logout.

## Definizione del Composable

**Posizione:** `src/composables/useAuth.js`

### Funzioni

- **login(user):** 
  - **Descrizione:** Effettua il login dell'utente, impostando il token di autenticazione e la compagnia corrente.
  - **Parametri:** 
    - `user`: Oggetto contenente le informazioni dell'utente (compresa la compagnia).
  - **Processo:**
    1. Imposta lo stato di caricamento nell'Auth Store.
    2. Imposta la compagnia corrente nello store Config e nel `localStorage`.
    3. Effettua una richiesta per ottenere un token di autenticazione.
    4. Aggiorna il token nell'Auth Store e lo stato di caricamento.
    5. Richiede i dati dell'utente attraverso il User Store.
  - **Ritorna:** La risposta dell'API con il token di autenticazione.
  - **Errori:** Gestisce errori di autenticazione e resetta lo stato.

- **logout():**
  - **Descrizione:** Effettua il logout dell'utente, rimuovendo i dati di autenticazione e la compagnia corrente.
  - **Processo:**
    1. Esegue il logout nell'Auth Store.
    2. Rimuove la compagnia corrente dallo store Config e dal `localStorage`.

### Utilizzo

Per utilizzare `useAuth`:

```javascript
import { useAuth } from '@/composables/useAuth';

const { login, logout } = useAuth();

// Esempio di login
await login({ username: 'user', password: 'pass', company: 'DEMO' });

// Esempio di logout
logout();
