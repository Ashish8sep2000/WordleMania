# WordleMania
A full-stack Wordle mobile app built with React Native and Expo, backed by a Django REST API.

# Full-Stack Wordle Mobile App (React Native + Django)

A beautiful, feature-rich Wordle clone designed as a cross-platform mobile application. This project features a clean Single Page Application (SPA) multi-screen workflow running on a mobile client, backed by a robust REST API for user authentication and persistence syncing.

## 📱 App Workflow & Architecture
The client application is built around an explicit multi-screen lifecycle state machine:
1. **App Launch ➔ Authentication Screen:** A secure username/password gateway that blocks unauthorized view access.
2. **Home Screen / Dashboard:** Hydrates the core interface with live tracking statistics pulled dynamically from the server.
3. **Wordle Engine Boot Sequence:** Tapping "Start Match" triggers the core engine loop:
   * **[Pull Stats]** ➔ Reads localized telemetry metrics.
   * **[Fetch Wordbank]** ➔ Asynchronously pulls an authentic dictionary corpus via an HTTP API request.
   * **[Setup UI Grid]** ➔ Instantiates a clean $6 \times 5$ grid matrix canvas and wipes historical virtual keyboard maps.

---

## 🛠️ Tech Stack
* **Frontend:** React Native, Expo Go (Framework), JavaScript ES6
* **Backend:** Django, Django REST Framework (DRF), SQLite/PostgreSQL
* **Authentication:** Django Token-Based Authentication
* **Local Caching:** LocalStorage / Async Storage state fallback

---