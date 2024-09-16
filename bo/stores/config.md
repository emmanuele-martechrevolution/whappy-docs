### `config.md`

````markdown
# Documentazione Config Store

Il Config Store fornisce dettagli di configurazione, inclusi gli URL API basati sulla compagnia corrente.

## Definizione dello Store

**Posizione:** `src/stores/config.js`

### Stato

- **API_URL:** Un oggetto contenente URL base per varie compagnie.
- **currentCompany:** Un `ref` che contiene il nome della compagnia corrente.

### Getters

- **getApiUrl:** Una proprietà `computed` che restituisce l'URL base per le richieste API in base alla `currentCompany`.
- **getSettingAddress:** Una proprietà `computed` che restituisce l'URL per l'endpoint API delle impostazioni.
- **getDriveAddress:** Una proprietà `computed` che restituisce l'URL per l'endpoint API del drive.

### Azioni

- **setCurrentCompany(company):** Imposta la compagnia corrente e aggiorna gli URL di conseguenza.

### Utilizzo

Per utilizzare il Config Store:

```javascript
import { useConfigStore } from "@/stores/config";

const configStore = useConfigStore();
configStore.setCurrentCompany("DEMO");
console.log(configStore.getApiUrl); // https://api-demo.whappy.it/api/
```
````
