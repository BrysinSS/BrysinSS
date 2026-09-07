# AIVS public sample provenance

## Selected source run

The public sample uses one lineage only:

| Field | Recorded value |
|---|---|
| Audit ID | `stage_h_product_replay_20260626_202930` |
| Audit timestamp | `2026-06-26T18:29:44Z` |
| Package schema | `client_audit_package/v3` |
| Stage H manifest schema | `stage_h_manifest/v2` |
| Measurement mode | `strict_production` |
| Measured language | `nl` |
| Queries × models | `27 × 4` |
| Valid responses | `108 / 108` |
| Providers | OpenAI, Google, Anthropic, Perplexity |

No local client path is published. The private source snapshot was inspected at Git commit `3809ab6ca006d397d58d65d3ea32927a3e0160e1`; the tracked v3/Stage H fixture lineage entered history at `f8bdc5bdbfb44b966b906f93b5d0a3de7fd74c1e`.

## Hash chain

The source package records `sha256:cf5f861e121affc9c924786f50ee2c0d352aa4c8f8f93c1f4742ee6ff6ad5fca` as the canonical package digest with the root `audit_attestation` block removed. Recomputing that digest with the private implementation produced the same value. Both saved Stage H manifests reference that same digest and audit ID.

The tracked JSON file's byte-level SHA-256 is `6fb0bd1b10a6d5dd08c31e019e18c7895bfb00a852b939bb80fa7e5f494e2256`. This differs from the canonical package digest because the file digest includes the attestation block and JSON serialization bytes.

The public files have their own byte-level hashes in [the public artifact manifest](sample/artifact_manifest.json). Those hashes establish integrity of this sanitized derivative; they do not recreate the private package signature.

## Stage H evidence

Two saved Stage H manifests, for Dutch and Russian output, both record:

- status `success` and final client artifacts emitted;
- package schema v3 and the same source package digest;
- presentation validation `pass`, with 0 errors and 0 warnings;
- checklist validation `pass`, with 0 errors and 3 warnings;
- original presentation and checklist PDF status `skipped`.

The final Dutch and Russian HTML files are tracked. Internal fact packs, marketing briefs, drafts and detailed validation JSON were referenced through temporary working paths and are no longer present. Git history contains no corresponding client PDFs. The public PDFs were therefore generated again from sanitized, self-contained HTML content based on the saved final artifacts and source metrics.

## Attestation state

The source package contains an Ed25519 attestation block. The canonical `package_sha256` value recomputes successfully, but signature verification returned `public_key_unavailable_for_public_key_id`. The saved Stage H manifest consequently records `signed: false` and `attestation_verified: false`.

This case study claims that an attestation is present. It does not claim that this source run's signature was independently verified.

## v3/v4 resolution

A later v4 regression rebuild exists with a different audit ID, 32 queries, 128 responses and different metrics and claim counts. Its production-readiness report is `partial`, with a soft competitor-profile coverage warning, and no matching final Stage H client artifacts were found. None of its values are used in this sample.

The selected v3 lineage is the only one that connects the 27-query measurement, 108 valid responses, 58/22/5 claim summary and saved Stage H delivery manifests.
