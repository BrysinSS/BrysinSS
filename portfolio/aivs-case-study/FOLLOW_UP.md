# AIVS evidence follow-up

These items were discovered while constructing the public sample. They are recorded here because fixing them would require changing or rerunning the private production system, which was outside this portfolio update.

- The original run directory named by the v3 package is no longer present in the current private checkout or the other available storage locations.
- Stage H manifests reference temporary fact packs, marketing briefs, drafts and detailed validation JSON that are no longer present. The tracked final HTML and manifests remain.
- No original client PDF exists in the current tree or any reachable Git revision. Stage H explicitly records PDF generation as `skipped`; the public PDFs are newly rendered sanitized derivatives.
- The legacy v3 root `audit_hash.content_hash` does not match recomputation by the current v5-era hash function. The separate attestation `package_sha256` does recompute and matches both Stage H manifests. The public provenance relies on that matching digest and does not claim the legacy root hash is currently valid.
- The v3 attestation public key is unavailable in the current environment. Presence is proven; signature verification is not.
- The saved manifests report three checklist warnings but the detailed validation files needed to classify those warnings are absent.
- A later v4 regression rebuild has no matching final Stage H artifacts and has a soft competitor-profile coverage warning. It was excluded to prevent cross-run metric mixing.
- A sandboxed pytest attempt could not maintain writable temporary directories. The authoritative test result was obtained in an unrestricted local run using the same commit and command.
