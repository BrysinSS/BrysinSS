# AIVS architecture

## Verified design

The commercial system is an eight-stage AI visibility audit pipeline. Every stage has specifications, gates and checks. Deterministic extraction is combined with LLM reasoning; guardrails classify claims and block unsupported or forbidden output.

The [overview diagram](README.md#eight-stage-pipeline) uses stage numbers. The separate public mapping repository's module registry must not be substituted for the private system's architecture.

## Responsibility boundaries

| Boundary | Public fact | Detail not supplied |
|---|---|---|
| Extraction / reasoning | Deterministic extraction and LLM reasoning coexist | Stage assignment and internal contracts |
| Stage validation | Specifications, gates and checks at every stage | Thresholds, schemas, recovery rules |
| Claims / evidence | Unsupported claims are blocked | Evidence representation and scoring |
| Reporting | Six output languages: ru, en, fi, de, nl, fr | Only Dutch was measured in the selected run |
| Delivery | Stage H renders and validates presentation/checklist artifacts | Saved detailed validation files are unavailable |
| Integrity | Canonical SHA-256 digest and Ed25519 attestation block | The selected run's signature was not verified because its public key was unavailable |

## Engineering decisions

Separating extraction from model reasoning makes each responsibility inspectable in its own terms. Stage gates provide checkpoints, and claim guardrails establish an evidence requirement. These are design implications of the confirmed features, not measurements of accuracy, latency or coverage.

## Reproducibility boundary

This portfolio does not include the executable, model configuration, input corpus or environment lockfiles. Readers can inspect a [sanitized production sample](sample/README.md), its [provenance](PROVENANCE.md) and the suite result, but cannot reproduce a commercial audit from these files. No claim of bit-for-bit identical LLM output is made.
