### `user.md`

````markdown
# User Store Documentation

The User Store manages user-related data, including fetching user details from the API.

## Store Definition

**Location:** `src/stores/user.js`

### State

- **status:** A `ref` holding the status of the user data fetching operation.
- **user:** A `ref` holding the user data.
- **loaded:** A `ref` indicating whether the user data has been loaded.

### Actions

- **fetchUser():** Fetches user data from the API and updates the `user` state. Logs out the user if an error occurs.
- **resetUser():** Resets the user data and status.

### Usage

To use the User Store:

```javascript
import { useUserStore } from "@/stores/user";

const userStore = useUserStore();
userStore.fetchUser();
console.log(userStore.user); // User data
```
````
