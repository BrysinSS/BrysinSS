# Sanitized AIVS production sample

This directory contains a public, reduced derivative of one production audit completed on 26 June 2026. It demonstrates the measurement contract, aggregate metrics, claim classification and Stage H delivery checks without exposing client material.

> Sanitized from a real production audit. Identifying business information and competitor names were removed; retained numeric engineering metrics are unchanged unless explicitly noted.

## Contents

| Artifact | Purpose |
|---|---|
| [Audit summary](sample_audit_summary.json) | Run scope, providers, language, completion and attestation state |
| [Metrics](sample_metrics.json) | Overall, interval, per-model and query-type measurements |
| [Claim verification](sample_claim_verification.json) | Aggregate claim-status counts |
| [Stage H validation](sample_stage_h_validation.json) | Saved delivery and validation results |
| [Presentation PDF](sample_audit_presentation.pdf) | Sanitized decision presentation |
| [Implementation checklist PDF](sample_implementation_checklist.pdf) | Sanitized implementation controls |
| [Presentation HTML](sample_presentation.html) | Accessible source for the public presentation |
| [Checklist HTML](sample_checklist.html) | Accessible source for the public checklist |
| [Artifact manifest](artifact_manifest.json) | SHA-256 and byte length for every public sample file |

The original Stage H run saved final HTML and recorded both PDF outputs as `skipped`. The two PDFs here were re-rendered as sanitized public derivatives. They are not the missing original client PDFs and do not carry the source package's Ed25519 signature.

The sample omits query text, model response text, URLs, contact details, evidence excerpts, implementation task text, client and competitor identities, prompts, commercial rules and signing material. See [provenance](../PROVENANCE.md) for the source-to-public lineage and its limits.
