# Kivi — verified build status

This repository contains the **financial intelligence engine**, **personality content**, **screen contracts**, and **product specification** as source packages. It is not yet a complete Android application.

## Verified locally on 24 October 2026
- The financial intelligence archive extracts successfully.
- Python standard-library regression suite: **91 tests passed**.
- The engine includes a local-only HTTP API and a basic HTML interface.
- The API is **not** internet-safe: no authentication, TLS, production tenancy, or secure provider credential handling.

## Still required before claiming a finished APK
1. Extract and organize Python source into version-controlled files.
2. Implement native Android UI from screen contracts and approved moodboard.
3. Implement Android SMS permission, inbox ingestion and transaction review.
4. Securely bridge Android and backend; avoid embedding any provider secrets.
5. Implement full transaction/history read APIs and missing financial edge cases.
6. Add account aggregator consent flow, only with properly configured server credentials.
7. Connect personality engine, receipt export, notifications and chat to verified financial data.
8. Run end-to-end tests, sign an Android APK, and test it on a physical device.

## Quick local run
```bash
python -m zipfile -e Kivi_Integrated_Financial_Intelligence_v1.zip build
cd build/kivi
python -m unittest discover -s tests -q
python -m kivi_engine.api
```
Visit http://127.0.0.1:8765 on the same computer.

**Do not expose the development server to the public internet.**
