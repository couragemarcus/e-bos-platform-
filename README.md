# e-BOS 2 — Free local business operations

A public catalog and customer inbox with a staff workspace for orders, stock, invoices, manually recorded payments, reports, people, equity, audit history and account security. The default installation needs no paid AI account, API key or subscription.

## Start on your computer

Install **Node.js 24** and **Podman Desktop**, then enable its Compose engine. From this extracted folder:

```sh
node scripts/configure.mjs
podman compose up --build -d
```

Open **http://localhost:3000/account.html**, create your owner account and save the company ID shown. Sign in at **http://localhost:3000/e-bos-backoffice.html**. Your first business is created automatically. The storefront is **http://localhost:3000/**.

Docker Engine with Compose also works with the same files: replace `podman compose` with `docker compose`. Podman is the default free desktop option. Internet is needed initially to download software and images; after setup the built-in assistant and business workflows run locally.

## What is included

- Owner registration; staff accounts; password changes and time-limited email resets; immediate session revocation; account disabling.
- Scoped owner, partner and worker permissions, including protection against staff privilege escalation.
- Materials and catalog publication, customer conversations, explicit human handoff and staff replies.
- Stock receipts/adjustments, movement history, low-stock thresholds and completion-driven inventory updates.
- Line-item totals, duplicate-safe order completion, printable invoices, manually checked cash/Mobile Money/bank records, and owner-authorized payment corrections.
- CSV exports, exact monetary aggregation, reports, activity audit history and in-app notifications.
- Free local text-guide retrieval and a deterministic automated assistant. Optional Ollama runs a downloaded model locally.
- Local email capture with Mailpit, daily backup files with retention, an optional Caddy HTTPS configuration, installable-app metadata and an offline notice that never queues payments.

**Payment records do not charge or verify money automatically.** Mailpit captures local emails rather than delivering them to the internet. Optional local-model answers need human checking. Software is free; your hardware, electricity, internet, public hosting and transaction-provider fees are separate.

## Documentation

| File | Contents |
| --- | --- |
| [SETUP.md](SETUP.md) | Windows/local installation, upgrading, optional services, commands and troubleshooting |
| [docs/PROCESSES.md](docs/PROCESSES.md) | End-to-end user and business workflows |
| [docs/FREE_STACK.md](docs/FREE_STACK.md) | Free components, sources, optional model and cost boundaries |
| [docs/SECURITY.md](docs/SECURITY.md) | Permissions, data protection, privacy and deployment boundaries |
| [docs/BACKUP_RESTORE.md](docs/BACKUP_RESTORE.md) | Backups, retention, fresh-cluster recovery and verification |
| [docs/API.md](docs/API.md) | New endpoints, payloads and status codes |
| [docs/VALIDATION.md](docs/VALIDATION.md) | Tests performed, results and unverified areas |
| [docs/CHANGELOG.md](docs/CHANGELOG.md) | Changes and migration notes |

Read the root documentation first. `backend/README.md` is a historical reference from the supplied project and describes superseded paid-provider paths and earlier validation claims.
