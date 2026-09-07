# AIVS security and traceability

## Confirmed controls

- Specifications, gates and checks at each of eight stages.
- Guardrails blocking claims without measurable foundations.
- Ed25519 attestation for reports.

## Attestation boundary

A signature verifies a specific payload against a public key. With a trusted key and a defined payload format, it can provide evidence of integrity and origin. It does not prove that a finding is true, that input is complete or that model reasoning is correct. Claim validation remains a separate responsibility.

This material includes no signing keys, verification tool, key-rotation procedure or attestation schema. It makes no claim about those implementation details.

## Traceability boundary

The confirmed guardrails require measurable support for claims. No specific storage model, immutable audit log, evidence identifier format or regulatory certification is asserted.

## Publication boundary

Only owner-approved facts are described. Private code, client documents, credentials, signing material, prompts and commercial rules are excluded. A file being present in another public repository does not establish that it is safe or representative of this system.

## Proposed verification artifact

An approved sanitized report with a public verification procedure would let readers inspect attestation without accessing the implementation. This is a proposed next step, not a currently shipped capability of this directory.
