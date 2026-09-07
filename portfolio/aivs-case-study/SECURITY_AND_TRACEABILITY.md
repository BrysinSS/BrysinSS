# AIVS security and traceability

## Evidence controls

- Stage contracts and validation gates separate collection, measurement, claim review and client delivery.
- Claim statuses distinguish verified facts, supported interpretations, hypotheses, unsupported claims and forbidden claims.
- The selected run's delivery summary contains 0 unsupported and 0 forbidden claims.
- A canonical package digest links the client package to both saved Stage H manifests.
- A separate public manifest records SHA-256 values for every sanitized sample artifact.

## Ed25519 status

The private package contains an Ed25519 attestation block. Presence alone is not verification. Its canonical package digest recomputes, but the corresponding public key was unavailable in the inspected environment. The source run is therefore documented as attestation present, `signed: false` and `attestation_verified: false`.

A valid signature would establish integrity and origin relative to a trusted public key. It would not prove that the crawl was complete, that a model answer was factually correct or that an interpretation was warranted. Those concerns remain with source quality, measurement design and claim validation.

## Sanitization boundary

The public sample removes the client and domain, URLs, phones, emails, addresses, people, response and query text, evidence excerpts, competitor identities, private paths, credentials, prompts, internal rules and signing material. Neutral labels such as `Client` and `Competitor A` are used only where structure needs an example.

Retained numeric metrics come from one v3 run. A later v4 rebuild is excluded. The public PDFs and HTML are sanitized derivatives and have their own public hashes; they do not inherit the private attestation.

See [provenance](PROVENANCE.md) for the exact digest relationship and [known evidence gaps](FOLLOW_UP.md) for unavailable historical artifacts.
