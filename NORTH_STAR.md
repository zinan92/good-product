# Good Product North Star

## Approved destination

Good Product is a public, Git-native collection of product and interface references that Park can search when building a product. Each catalog entry represents one product or tool and contains a real primary screenshot; it may also contain multiple gallery screenshots, a curator note, tags, a collection date, and an optional source link.

The content source is this repository. The public consumer is `park-ai-intel.com/goodproduct`, rendered by the separate `park-ai-intel` site repository.

## Non-negotiable boundaries

- Content-only repository: `manifest.yaml` plus `images/` are the source of truth.
- `kind: inspiration` means visual inspiration not yet validated; `kind: tool` means a tool or pattern Park has used and validated.
- Public by default, but sensitive/private material stops publication.
- No placeholder assets in the published collection; an entry without a real screenshot fails the content sync.
- No CMS, database, upload service, build pipeline, or deployment configuration in this repository.
- Do not manually edit `zinan92/park-operating-system` or `zinan92/product-lab`.

## Success condition

Park can add one screenshot and one manifest record with ordinary Git commands, and the main site can consume the content without a second data store.
