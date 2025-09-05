Flutter Developer — Take-Home Test Assignment

Goal: Build a small Flutter mini-app that implements a test crypto wallet (balance, transfers, tx history) and a one-to-one chat with push notifications. Deliver a working APK and push the full project to the given Git repo with README and documentation.

Requirements (must-have)

Crypto wallet (test)

Show account balance (use a testnet / mock API — see Implementation Notes below).

Send transfer: UI to enter recipient address, amount, and submit a transfer.

Transaction history: list recent transactions (status: pending / success / failed).

Manage a single account/private key inside the app (test/dev only). Do not connect to a live mainnet wallet or store real funds.

One-to-one chat

Implement 1:1 chat between two users.

Use Firebase Realtime Database / Firestore + Firebase Auth or a WebSocket backend. (Either option is acceptable — document which you used.)

Show messages in chronological order, support text messages at minimum.

Support real-time updates (incoming message appears without refresh).

Push notifications

Implement push notifications for incoming chat messages (Firebase Cloud Messaging recommended if using Firebase).

Notifications should open the chat on tap.

Delivery & repo

Push source code into the provided Git repository.

Include a README with:

How to run locally (install, env vars, Firebase / server setup)

How to build the APK

Any assumptions and known limitations

Include a documentation file describing architecture and design decisions (1–2 pages).

Provide a working APK file (debug or unsigned release is fine) inside the repo or attached to the PR.

Deadline

Send/push code and APK by Sunday or Monday morning before you come into the office (state the exact date/time in your submission).

Nice-to-have (bonus)

Use a simple, clean UI (Tailwind-like style equivalents in Flutter: tidy Material or a design system).

Offline message caching (show last messages when offline).

Unit/integration tests for at least one feature (wallet or chat).

Transaction status updates (simulate confirmations).

Use a small backend (Node/Python) for simulated blockchain operations if you didn’t use a public testnet.

Implementation notes & constraints (important)

Security: This is a test app — you may store keys in local storage for demo purposes, but do not hardcode private keys in the repo. Document storage choice in README.

Blockchain: You may either:

Connect to a public testnet (e.g., Sepolia / Goerli if available) using a public RPC provider (Alchemy/Infura) and show real balances on testnet; or

Implement a mock backend that simulates balances/transactions (acceptable and simpler). If you use a mock backend, provide endpoints and sample responses in your docs.

Chat backend: If you choose WebSocket, provide a small server repository or a Dockerfile so we can run it locally. If you choose Firebase, include the Firebase project config instructions or sample .env with placeholders.

APK: Building a debug APK is acceptable:

Build command: flutter build apk --debug (or flutter build apk --release if you sign).

Provide the built APK inside releases/ in repo (or attach in the PR).

Deliverables (what we expect in the repo)

Complete Flutter project source code.

releases/app.apk — working APK (debug is fine).

README.md — setup, run, build instructions, env/config.

DOCS.md — architecture diagram (text or image), design choices, APIs used, known limitations.

OPTIONAL: small server code if you used custom WebSocket/mock APIs.

A short bullet list in the PR description summarizing what was completed and any missing items.

Evaluation criteria (how we grade)

Functionality (50%) — Wallet flows (balance, send, history) and chat + push notifications work as described.

Code quality (20%) — Readable, modular, commented where needed.

Documentation (15%) — Clear README and DOCS explaining setup and design choices.

UX & polish (10%) — Usable UI, good error handling and input validation.

Bonus (5%) — Tests, offline support, extra polish.

Example repo structure (suggestion)
prism-miniapp/
├─ lib/
│  ├─ main.dart
│  ├─ screens/
│  │  ├─ wallet/
│  │  │  ├─ wallet_screen.dart
│  │  │  ├─ send_screen.dart
│  │  ├─ chat/
│  │  │  ├─ chat_list.dart
│  │  │  ├─ chat_screen.dart
│  ├─ services/
│  │  ├─ wallet_service.dart   # rpc/mock api
│  │  ├─ chat_service.dart     # firebase/ws
├─ android/
├─ ios/
├─ pubspec.yaml
├─ README.md
├─ DOCS.md
├─ releases/app.apk

Quick tips & common pitfalls

Do not process huge files or heavy jobs on the UI thread — keep network calls async.

For push notifications with Firebase, remember to configure the Android google-services.json.

If using testnet RPC providers like Infura/Alchemy, remember to add rate-limit handling and document how to create API keys.

Keep the private key handling minimal: generate a single demo account in-app on first run for ease of testing.

Submission instructions (explicit)

Push your code to the provided Git repo (branch prism-miniapp/<your-name>).

Add the APK to releases/ and commit it.

Open a PR or send a link to the repo and state the exact submission time (so we can confirm it met the deadline).

Include your README and DOCS explaining how to test the app (username/password or test account info).
