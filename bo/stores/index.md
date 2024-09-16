# Pinia Stores Documentation

In this project, we use Pinia as our state management library for Vue 3. This document provides an overview of the Pinia stores used in the application.

## Stores Overview

We have the following Pinia stores:

1. **Auth Store** (`auth`)
2. **Config Store** (`config`)
3. **User Store** (`user`)

Each store is responsible for managing specific parts of the application's state and providing necessary actions and getters for state management.

---

### Auth Store

- **Location:** `src/stores/auth.js`
- **Purpose:** Manages authentication state, including token handling and user login/logout functionality.

### Config Store

- **Location:** `src/stores/config.js`
- **Purpose:** Provides configuration details such as API URLs based on the current company.

### User Store

- **Location:** `src/stores/user.js`
- **Purpose:** Manages user data, including fetching user information from the API and resetting user state.

For detailed documentation on each store, refer to the individual store documentation files.
