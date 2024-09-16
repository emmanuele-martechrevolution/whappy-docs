# Documentazione User Store

Il User Store gestisce i dati relativi all'utente, inclusa la richiesta delle informazioni dell'utente dall'API.

## Definizione dello Store

**Posizione:** `src/stores/user.js`

### Stato

- **status:** Un `ref` che contiene lo stato dell'operazione di richiesta dei dati dell'utente.
- **user:** Un `ref` che contiene i dati dell'utente.
- **loaded:** Un `ref` che indica se i dati dell'utente sono stati caricati.

### Azioni

- **fetchUser():** Richiede i dati dell'utente dall'API e aggiorna lo stato `user`. Effettua il logout dell'utente se si verifica un errore.
- **resetUser():** Resetta i dati dell'utente e lo stato.

### Utilizzo

Per utilizzare il User Store:

```javascript
import { useUserStore } from "@/stores/user";

const userStore = useUserStore();
userStore.fetchUser();
console.log(userStore.user); // Dati dell'utente
```
