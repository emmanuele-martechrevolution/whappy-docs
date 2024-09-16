### `config.md`

````markdown
# Config Store Documentation

The Config Store provides configuration details, including API URLs based on the current company.

## Store Definition

**Location:** `src/stores/config.js`

### State

- **API_URL:** An object containing base URLs for various companies.
- **currentCompany:** A `ref` holding the current company name.

### Getters

- **getApiUrl:** A `computed` property that returns the base URL for API requests based on the `currentCompany`.
- **getSettingAddress:** A `computed` property that returns the URL for the settings API endpoint.
- **getDriveAddress:** A `computed` property that returns the URL for the drive API endpoint.

### Actions

- **setCurrentCompany(company):** Sets the current company and updates the URLs accordingly.

### Usage

To use the Config Store:

```javascript
import { useConfigStore } from "@/stores/config";

const configStore = useConfigStore();
configStore.setCurrentCompany("DEMO");
console.log(configStore.getApiUrl); // https://api-demo.whappy.it/api/
```
````
