# Good Product Decision Log

## 2026-08-30 — Add Subscrr

- Decision: add Subscrr as `GP-003`, classified as `inspiration`.
- Why: the supplied screen is a useful reference for combining a high-emotion landing visual with a concrete mobile product promise: translate recurring payments into daily, monthly, and yearly cost.
- Evidence: user-provided screenshot `images/subscrr-app.png` and source `https://subscrr.app/`.

## 2026-08-30 — Add Decathlon Yestalgia

- Decision: add Decathlon Yestalgia as `GP-002`, classified as `inspiration`.
- Why: the supplied screen is a strong reference for turning a retro sports capsule into a navigable brand story through art direction, composition, microcopy, and product browsing.
- Evidence: user-provided screenshot `images/decathlon-yestalgia.png` and source `https://decathlonyestalgia.com/fr/`.

## 2026-08-29 — Replace placeholders with the first real product

- Decision: remove the nine placeholder seed records and make NewsLiquid `GP-001`, with the three user-provided screenshots stored as one product gallery.
- Why: the collection is now starting its real content phase; a placeholder catalog obscures whether the public page contains actual product references.
- Decision: classify NewsLiquid as `inspiration` because the supplied material proves visual/product reference, not Park's independent validation of the tool in a workflow.
- Decision: keep `image` as the primary cover and add optional `images` for additional screenshots; the primary image must be repeated as the first gallery item.
- Evidence: `https://newsliquid.com/` and the three files under `images/newsliquid-*.png`.

### Gotchas

- The supplied screenshots include account/order-panel example values. They are treated as product demo data based on the public product context; do not add screenshots containing Park's private account or customer data without a separate privacy check.
- `pending.svg` is intentionally removed. Future content without a real screenshot must fail the sync rather than fall back to a public placeholder.

## 2026-08-29 — Establish the content source

- Decision: create `zinan92/good-product` as a public, content-only repository.
- Why: screenshots and curator notes are the durable asset; website code and deployment should remain in `park-ai-intel`.
- Decision: one entry represents one product or tool and can point to multiple future screenshots through the record/gallery model.
- Decision: seed the catalog with the nine records from the approved handoff mockup, using one explicit `images/pending.svg` placeholder until real screenshots arrive.
- Decision: the website consumes a local copy of this repository; no cross-Vercel rewrite, reverse proxy, database, or CMS.
- Decision: `product-lab` and `park-operating-system` are not edited manually; Product Lab indexing waits for the next canonical snapshot.

### Gotchas

- `manifest.yaml` is the only content metadata source. Do not create a second hand-maintained JSON catalog.
- Public-by-default does not mean publish blindly: private screenshots, credentials, customer data, or sensitive UI must stop the refresh.
- Keep `catalog_no` stable after publication; adding a new item appends the next number rather than renumbering older entries.
