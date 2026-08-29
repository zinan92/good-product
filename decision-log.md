# Good Product Decision Log

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
