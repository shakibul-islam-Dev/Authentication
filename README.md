# Raw Node.js Uptime Monitoring API

A production-grade, highly performant Uptime Monitoring API built entirely from scratch using **Raw Node.js**. This project intentionally avoids Express or any third-party `npm` modules to leverage the full power of Node.js built-in core modules.

---

## 🚀 Features

- **Raw Node.js Architecture**: Built using native modules (`http`, `crypto`, `fs`, `path`, etc.) with zero external npm dependencies.
- **RESTful API**: Standardized CRUD operations for handling users, tokens, and monitoring checks.
- **Authentication & Authorization**: Secure token-based authentication system generated and verified using native cryptography.
- **User Management**: Complete system for user signup, profile updates, and setting configurations.
- **Uptime Tracking System**: Background workers that automatically perform periodic HTTP/HTTPS checks on user-defined URLs.
- **SMS Notifications**: Real-time alerts sent directly to user phones when a monitored site goes up or down, powered by the **Twilio API**.

---

## 🛠️ Built With

- **Node.js Core Modules**:
  - `http` & `https` – For creating the server and handling external ping requests.
  - `crypto` – For hashing passwords and managing authentication tokens.
  - `fs` & `path` – For standard file-system data storage (JSON-based flat files).
  - `string_decoder` – For handling incoming data streams.
- **Third-Party Services**:
  - **Twilio API** – For sending SMS notifications.

---

## ⚙️ Prerequisites

- **Node.js** (v14.x or higher recommended)
- A **Twilio** account to obtain credentials for SMS alerts.

---

## 📂 Project Structure

```text
├── .env                  # Environment configurations
├── lib/                  # Core logic libraries
│   ├── data.js           # File system CRUD operations
│   ├── helpers.js        # Hashing, Twilio SMS integration, parsing
│   ├── server.js         # HTTP server and request router
│   └── workers.js        # Background uptime check runners
├── handlers/             # Request handlers
│   ├── userHandler.js    # User CRUD
│   ├── tokenHandler.js   # Authentication tokens
│   └── checkHandler.js   # Monitoring configuration
├── .data/                # Flat-file database storage (JSON)
└── index.js              # Project entry point
```
