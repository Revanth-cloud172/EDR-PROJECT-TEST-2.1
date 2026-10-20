# Security model and limitations

This project is a student-facing security demonstration.

## Included controls

- No user-supplied strings are injected as HTML without escaping in table renderers.
- No external scripts, stylesheets, or CDN dependencies.
- Web Crypto API for SHA-256 and ECDSA P-256 signing demonstrations.
- Local export lets analysts preserve a JSON snapshot manually.

## Not production controls

- Browser local storage is not a trusted evidence vault.
- A hash chain detects changes relative to retained hashes, but cannot prove authenticity if an attacker controls all data.
- There is no server authentication, server-side access control, immutable storage, remote audit log, hardware trust anchor, device attestation, or secure boot.
- Do not use for real vehicle safety, legal evidence, or operational crash recording.
