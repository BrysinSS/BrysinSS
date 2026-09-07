# Stanislav Brysin
**AI Automation Engineer**

Python | n8n | APIs | LLM workflows | Testing | CI/CD | Data pipelines

[GitHub](https://github.com/BrysinSS) · [Portfolio](README.md)

## Profile

I build automation systems using Python, APIs, n8n and LLM integrations, with an emphasis on deterministic processing, structured data, testing and reproducible pipelines. My background includes approximately eight years independently running a manufacturing business. I am seeking automation and applied AI engineering roles in the Netherlands.

## Selected engineering work

### AIVS — commercial AI visibility auditing system

- Built an automated eight-stage audit pipeline with specifications, gates and checks at every stage.
- Combined deterministic extraction with LLM reasoning.
- Implemented evidence-based claim gates and Ed25519 package attestation, with signature presence and verification reported separately.
- Verified the private suite at 4,308 passed, 12 skipped and 0 failed tests (4,320 collected; September 2026).
- Delivered a strict-production audit across 27 Dutch queries and four model providers: 108/108 valid responses, with 0 unsupported and 0 forbidden claims in the final package.
- Built client report output for six languages; the documented production sample measured Dutch and produced validated Dutch and Russian artifacts.

[Case study](portfolio/aivs-case-study/README.md) · [sanitized production sample](portfolio/aivs-case-study/sample/README.md) · [test record](portfolio/aivs-case-study/TESTING.md). The implementation remains private; the public evidence includes run metrics, Stage H validation and provenance hashes.

### AI Accountant Orchestra — Python transaction processing

- Built a YAML-driven deterministic recipe engine with CSV normalization, summaries, JSON/Markdown artifacts and NDJSON step logs.
- Implemented VAT/BTW and simplified KOR calculation functions, with eight existing pytest tests covering selected loading, grouping and tax behavior.
- Configured GitHub Actions to run tests. Documented the limits of the bundled summary recipe and validation behavior.

### Research automation — Literature Parser and PDF Hunter

- Built an n8n workflow for Crossref/OpenAlex metadata collection, normalization and DOI/title deduplication.
- Built a Python resolver using official metadata APIs and document endpoints with explicit PDF source priority and structured CSV output.
- Documented the file-based handoff, DOI-format limitations and source-failure behavior.

## Business background

Independently ran a manufacturing business for approximately eight years.

## Technical skills

Python, n8n, APIs, YAML, structured data, data pipelines, LLM integrations, deterministic/AI hybrid workflows, pytest and GitHub Actions / CI. The public repositories demonstrate CI; a deployed continuous-delivery pipeline is not claimed.

Development tools: Claude Code and Codex, used for AI-assisted development.

## Draft completion notes — remove before sending

This is a content draft, not a complete employment chronology. Contact details, dates, business name, education, location, work authorization and language levels were not supplied. No language level has been added or changed. See PORTFOLIO_REPORT.md for NEEDS_USER_CONFIRMATION items.
