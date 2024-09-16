# Documentazione Auth Store

L'Auth Store è responsabile della gestione dello stato di autenticazione dell'utente.

## Definizione dello Store

**Posizione:** `src/stores/auth.js`

### Stato

- **token:** Un `ref` che contiene il token di autenticazione, recuperato da `localStorage` se disponibile.
- **status:** Un `ref` che contiene lo stato dell'autenticazione (ad es. successo, errore).
- **hasLoadedOnce:** Un `ref` che indica se lo store è stato caricato almeno una volta.

### Getters

- **isAuthenticated:** Una proprietà `computed` che restituisce `true` se il `token` non è vuoto.
- **authStatus:** Una proprietà `computed` che restituisce lo stato corrente dell'autenticazione.

### Azioni

- **setToken(newToken):** Imposta un nuovo token di autenticazione e aggiorna `localStorage` e le intestazioni di `axios`.
- **setStatus(newStatus):** Aggiorna lo stato di autenticazione.
- **setHasLoadedOnce(loaded):** Aggiorna lo stato di `hasLoadedOnce`.
- **logout():** Cancella il token, lo stato e `hasLoadedOnce`, rimuove il token da `localStorage` e elimina l'intestazione `Authorization` da `axios`.

### Utilizzo

Per utilizzare l'Auth Store:

```javascript
import { useAuthStore } from "@/stores/auth";

const authStore = useAuthStore();
authStore.setToken("nuovo-token");
console.log(authStore.isAuthenticated); // true o false
```
