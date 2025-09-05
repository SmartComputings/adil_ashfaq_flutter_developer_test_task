````markdown
# 💰 Mini Crypto App (prism-miniapp)

## 📌 Overview
This is a **test assignment Flutter mini-app** for a developer evaluation.  
The app demonstrates two main features:

1. **Crypto Wallet (Test)**
   - View balance
   - Send transfer
   - Transaction history

2. **One-to-One Chat**
   - Real-time messaging (Firebase or WebSocket)
   - Push notifications for new messages

The candidate must build, document, and deliver the app with an **APK** and source code.

---

## ✅ Requirements

### Crypto Wallet
- Show test account balance (use mock/testnet APIs).
- Send transfers to another account.
- Transaction history with statuses: *pending / success / failed*.

### One-to-One Chat
- Chat between two users.
- Real-time updates via Firebase or WebSocket.
- Push notifications for incoming messages.
- Notifications should open the chat screen.

### Delivery
- Push **full source code** into this repo.
- Add a working **APK** inside `releases/app.apk`.
- Provide:
  - `README.md` → setup & build instructions  
  - `DOCS.md` → architecture, design choices, APIs used  

### Deadline
Submit by **Sunday night / Monday morning before office**.

---

## 📂 Project Structure

```text
prism-miniapp/
├─ lib/
│  ├─ main.dart                 # App entry point
│  ├─ screens/
│  │  ├─ wallet/                # Wallet UI
│  │  │  ├─ wallet_screen.dart
│  │  │  ├─ send_screen.dart
│  │  ├─ chat/                  # Chat UI
│  │  │  ├─ chat_screen.dart
│  │  │  ├─ chat_list.dart
│  ├─ services/
│  │  ├─ wallet_service.dart    # Wallet logic (API/testnet/mock)
│  │  ├─ chat_service.dart      # Chat logic (Firebase/WebSocket)
│  ├─ utils/                    # Helpers, constants, configs
├─ android/                     # Android project files
├─ ios/                         # iOS project files
├─ releases/app.apk             # Final APK output
├─ README.md                    # Setup instructions
├─ DOCS.md                      # Architecture & documentation
````

---

## ⚙️ Getting Started

### Clone the repo

```bash
git clone <your-repo-url>
cd prism-miniapp
```

### Install dependencies

```bash
flutter pub get
```

### Run the app

```bash
flutter run
```

### Build APK

```bash
flutter build apk --debug
# APK will be generated at:
# build/app/outputs/flutter-apk/app-debug.apk
```

Move/copy the APK into:

```
releases/app.apk
```

---

## 📝 Notes

* Use **mock APIs** or **testnet RPC providers** for wallet — no real funds.
* Either **Firebase** or a **custom WebSocket server** can be used for chat.
* Push notifications should open the chat screen.
* Document all assumptions in `DOCS.md`.

---

## 🔍 Evaluation Criteria

* **Functionality (50%)** — Wallet + chat features working.
* **Code Quality (20%)** — Clean, modular, maintainable.
* **Documentation (15%)** — Clear README + DOCS.
* **UX & Error Handling (10%)** — Smooth, user-friendly flow.
* **Bonus (5%)** — Tests, offline mode, polished UI.

---

## 📧 Submission

* Push **code + APK + docs** to this repository.
* Ensure APK is available in: `releases/app.apk`.
* Deadline: **Sunday night / Monday morning before office**.

---

```
