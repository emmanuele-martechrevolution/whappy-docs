# Auth Store Documentation

The Auth Store is responsible for managing the authentication state of the user.

## Store Definition

**Location:** `src/stores/auth.js`

### State

- **token:** A `ref` holding the authentication token, retrieved from `localStorage` if available.
- **status:** A `ref` holding the status of the authentication (e.g., success, error).
- **hasLoadedOnce:** A `ref` indicating whether the store has been loaded at least once.

### Getters

- **isAuthenticated:** A `computed` property that returns `true` if the `token` is not empty.
- **authStatus:** A `computed` property that returns the current authentication status.

### Actions

- **setToken(newToken):** Sets a new authentication token and updates `localStorage` and `axios` headers.
- **setStatus(newStatus):** Updates the authentication status.
- **setHasLoadedOnce(loaded):** Updates the `hasLoadedOnce` state.
- **logout():** Clears the token, status, and `hasLoadedOnce` state, removes the token from `localStorage`, and deletes the `Authorization` header from `axios`.

### Usage

To use the Auth Store:

```javascript
import { useAuthStore } from "@/stores/auth";

const authStore = useAuthStore();
authStore.setToken("new-token");
console.log(authStore.isAuthenticated); // true or false
```
