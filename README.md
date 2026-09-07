# Stanislav Brysin
**AI Automation Engineer**

I build reliable automation systems using Python, APIs, n8n and LLMs, with deterministic logic, testing and reproducible pipelines.

## What I build

- Data pipelines that turn raw inputs into structured, inspectable outputs.
- API integrations and n8n workflows for research and business automation.
- Hybrid workflows combining deterministic processing and LLM reasoning.

## Engineering principles

Make input and output contracts explicit. Separate deterministic processing from model reasoning. Validate intermediate results, preserve evidence and make failures visible. Use tests and CI to check behavior; document implementation limits.

## Featured projects

### AIVS — AI visibility auditing

**Problem:** Make AI visibility audits repeatable and evidence-backed.

**What I built:** An eight-stage audit pipeline combining deterministic extraction and LLM reasoning, with specifications, gates and checks at every stage.

**Engineering highlights:** A real strict-production run completed 108/108 model responses across four providers; claim gates produced 0 unsupported and 0 forbidden claims. The private suite currently records 4,308 passed and 12 skipped tests. Client reports support six output languages; this run measured Dutch.

**Evidence:** [Commercial system case study](portfolio/aivs-case-study/README.md), [sanitized production sample](portfolio/aivs-case-study/sample/README.md), [provenance](portfolio/aivs-case-study/PROVENANCE.md), [architecture](portfolio/aivs-case-study/ARCHITECTURE.md) and [testing](portfolio/aivs-case-study/TESTING.md). The implementation remains private; the public package exposes sanitized metrics, validation outcomes and hashes.

### AI Accountant Orchestra — configurable transaction processing

**Problem:** Make CSV transaction processing repeatable and inspectable.

**What I built:** A Python recipe engine that loads, normalizes and summarizes transactions through YAML-defined steps.

**Engineering highlights:** NDJSON logs, JSON/Markdown artifacts, separately tested VAT/BTW and simplified KOR calculations, pytest and GitHub Actions. The bundled BTW recipe is a summary demo with fixed tax metadata.

**Evidence:** [Project and quick start](https://github.com/BrysinSS/ai-accountant-orchestra), [tests](https://github.com/BrysinSS/ai-accountant-orchestra/tree/main/tests), [CI](https://github.com/BrysinSS/ai-accountant-orchestra/actions/workflows/ci.yml).

### PDF Hunter — open-access PDF resolution

**Problem:** Find PDF links across several sources without scraping publication pages.

**What I built:** A Python resolver that reads article JSON and writes CSV results using three metadata APIs and two official document endpoints.

**Engineering highlights:** Explicit source priority, typed result models and per-source failure isolation. Selection is deterministic for fixed upstream responses; live availability changes.

**Evidence:** [Project](https://github.com/BrysinSS/pdf-hunter-python), [selection logic](https://github.com/BrysinSS/pdf-hunter-python/blob/main/src/merge_logic.py), [recorded output](https://github.com/BrysinSS/pdf-hunter-python/blob/main/output/articles_pdf_results.csv). No automated suite or CI is included yet.

### Literature Parser — research metadata workflow

**Problem:** Collect publication metadata for several research topics in a common format.

**What I built:** An n8n workflow that queries Crossref and OpenAlex, normalizes records, merges results and applies DOI/title deduplication.

**Engineering highlights:** Exportable workflow, source attribution and structured JSON compatible with PDF Hunter's input wrapper. DOI normalization remains a documented integration limitation.

**Evidence:** [Project, workflow and screenshot](https://github.com/BrysinSS/literature-parser-n8n).

Additional source example: [Declarative Business JSON-LD](https://github.com/BrysinSS/declarative-business-jsonld), a public declared-data mapping project distinct from the commercial AIVS system.

## Core stack

Python · n8n · APIs · data pipelines · YAML · structured data · LLM integrations · pytest · GitHub Actions / CI

AI-assisted development tools: Claude Code and Codex. Engineering evidence is in the implementations, contracts, tests and documented limitations linked above.

## Background

I independently ran a manufacturing business for approximately eight years. My focus is now AI automation engineering, with an emphasis on practical business workflows and verifiable systems.

## Contact

[GitHub: BrysinSS](https://github.com/BrysinSS). Open to AI Automation Engineer, Automation Developer, Applied AI Engineer and Python Automation Engineer roles in the Netherlands.
