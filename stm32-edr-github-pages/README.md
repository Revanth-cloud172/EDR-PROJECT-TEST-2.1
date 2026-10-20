# STM32 EDR Security & Forensic Simulator — GitHub Pages

This edition is a **static, browser-only application** designed to run from GitHub Pages. It does not need a Python backend, server, database service, API token, build step, or external JavaScript dependency.

## Deploy

1. Create a GitHub repository.
2. Upload the project files and folders, keeping their paths unchanged.
3. Commit to the `main` branch.
4. Open **Settings → Pages**.
5. Under build and deployment, choose **Deploy from a branch**, then select `main` and `/(root)`.
6. Save and wait for GitHub Pages to publish the site. Open the URL shown in Settings → Pages.

The included GitHub Actions workflow also checks that the static entry point and asset files exist; it does not require secrets.

## Use

- Start simulation or add a sample.
- Trigger an incident to snapshot recent telemetry.
- Generate an ECDSA P-256 browser key pair and sign/verify a challenge.
- Verify the SHA-256 evidence chain.
- Simulate a record modification, then verify again.
- Export the forensic bundle as JSON.

## Important limitations

- Telemetry is simulated; no STM32/ESP32 device is connected.
- Data is stored in this browser's local storage. It does not synchronize between browsers/users, and clearing browser storage deletes the local copy. Export JSON backups.
- The hash chain is a teaching demonstration. An attacker who can rewrite all local storage can rewrite the chain; this is not production-grade tamper-proof storage.
- ECDSA key is browser-local and non-extractable; it is not a server identity and is not used to attest incident data.
- GitHub Pages is static hosting only. For shared accounts, authenticated users, central persistence, server-side key custody, or device ingestion, a separate backend is required.
