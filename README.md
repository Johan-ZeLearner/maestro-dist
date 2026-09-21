# Maestro — update distribution

Public download channel for [Maestro](https://github.com/eg-sandbox/maestro)'s
in-app auto-updater. This repository holds **only release artifacts** — no source.

Each release carries three files:

- `latest.json` — the update feed the app polls
- `Maestro.app.tar.gz` — the packaged app bundle
- `Maestro.app.tar.gz.sig` — its ed25519 signature

## Is a public host safe?

Yes. Every installed copy of Maestro verifies each download against a public key
compiled into the app, so a tampered or forged bundle is rejected. The host only
needs to be reachable — the signature, not this repository, is what guarantees
integrity. The application source stays private.

Artifacts here are published automatically by Maestro's release CI; manual edits
aren't expected.
