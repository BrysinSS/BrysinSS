# Portfolio audit

Audit date: 7 September 2026. Scope: the default branches of the five repositories below, inspected before editing. All five are public. No private repository was accessed. Evidence paths refer to the original checkout; validation results and source revisions are recorded in PORTFOLIO_REPORT.md.

P0: undermines trust. P1: materially weakens the portfolio. P2: useful improvement.

| Issue | Repository | Severity | Evidence | Recommended fix |
|---|---|---|---|---|
| Profile omits name, featured case evidence, background and contact link | BrysinSS | P1 | README.md is a short list without clickable project links | Lead with role and link each case to inspectable evidence |
| Invalid CI badge, clone placeholder and unclosed installation fence | ai-accountant-orchestra | P0 | README.md:2,59; opening bash fence never closed | Correct URL and write executable, separate commands |
| CLI dependency absent from installation manifest | ai-accountant-orchestra | P0 | ui/cli.py imports rich; requirements.txt omits it; main.py fallback can return OK without business execution | Add rich and verify real CLI import and recipe artifacts |
| BTW recipe does not calculate VAT or filter transactions by period | ai-accountant-orchestra | P0 | recipes/btw_return.yml calls summarize, hardcodes kor_applied and zero vat_breakdown; no compute_vat step | Describe it as a summary demonstration; document separately tested VAT/KOR functions |
| Validation report does not enforce a gate | ai-accountant-orchestra | P1 | tools/validation/schema.py returns valid/errors; controller does not interpret valid=false | Explain current validation boundary; plan a separate behavior change |
| Agent step is a no-op and natural-language parsing uses regex | ai-accountant-orchestra | P1 | orchestrator/controller.py agent branch; agents/accountant_agent.py | Avoid claiming implemented LLM accounting or autonomous agents |
| Exit code alone does not establish success | ai-accountant-orchestra | P1 | ui/cli.py returns 0 after printing a result; main.py fallback returns 0 | Tell readers to inspect result status, logs and artifacts |
| Existing tests cover selected functions, not end-to-end accounting | ai-accountant-orchestra | P1 | tests/test_loader.py, test_bookkeeping.py, test_tax.py contain eight tests | State exact coverage; link CI rather than claiming a full suite |
| Source list omits Zenodo; not every adapter calls an API | pdf-hunter-python | P1 | src/pdf_hunter.py; arXiv/HAL adapters use HEAD against document endpoints | List five sources and distinguish API calls from document checks |
| Reproducibility claim needs an upstream-data boundary | pdf-hunter-python | P1 | merge_logic.py has fixed priority; fetchers use live HTTP | Describe deterministic selection for fixed responses |
| Failures are indistinguishable from missing PDFs | pdf-hunter-python | P1 | fetchers catch exceptions; merge_logic.py returns not found | Document failure behavior and lack of diagnostics/retries |
| Unpaywall uses a placeholder email | pdf-hunter-python | P1 | src/fetch_unpaywall.py EMAIL | Replace with environment configuration; document setup |
| DOI URL prefixes are retained; canonical_doi is unused in lookup | pdf-hunter-python | P1 | load_articles, fetch_s2.py, fetch_unpaywall.py | Document bare-DOI requirement; defer normalization logic change |
| No test suite, CI, license or dependency pins | pdf-hunter-python | P1 | Tracked file inventory and requirements.txt | State gaps; avoid inventing license or passing-test claims |
| Example input/output exists but is not surfaced | pdf-hunter-python | P1 | input/articles.json; output/articles_pdf_results.csv | Quote a real matching excerpt and link full files |
| Documented file paths do not exist | literature-parser-n8n | P0 | README lists workflow/parser.json and docs/workflow-preview.png; actual files are at repository root | Correct links and embed existing screenshot |
| Deduplication is partial | literature-parser-n8n | P1 | DedupArticles lowercases/trims DOI but does not strip doi.org prefix; first metadata/topic retained | Explain exact keys and data loss boundary |
| No-credentials and fully-automated claims overstate export | literature-parser-n8n | P1 | Manual trigger, HTTP nodes without credentials, Convert to File without storage node | Document manual run/download and check current provider access requirements |
| Workflow has no automated tests, CI, version pin or license | literature-parser-n8n | P1 | Tracked file inventory | State status and manual acceptance procedure |
| Public AIVS snapshot and commercial AIVS need separate evidence | AIVS-Declarative-Pipeline | P0 | README describes declarative mapping; reporting/optimization code includes stubs; no 4300-test suite or Ed25519 implementation present | Separate public code from owner-confirmed commercial case study |
| Boundary and CLI contracts disagree | AIVS-Declarative-Pipeline | P0 | test_g2_c1.py imports missing run_pipeline; CLI sends --client/--output-json while core accepts --client_id and prints status text | Record failure; offer only a directly checked mapping example |
| JSON-LD conformance and 100% traceability claims exceed evidence | AIVS-Declarative-Pipeline | P1 | structured_data/run.py maps fields but has no schema.org validation; confirmation modules include placeholders | Describe mapping, not validated conformance or full enforcement |
| Missing dependency manifest, CI and license | AIVS-Declarative-Pipeline | P1 | PDF parser imports PyPDF2; no install manifest or workflow | State reproducibility gaps; avoid claiming runnable full pipeline |
| Existing client-like samples are not proven sanitized | AIVS-Declarative-Pipeline | P1 | input/, output/, delivery/ contain business-shaped records and archives | Do not republish in case study; request a sanitized report |
| Tracked bytecode and IDE metadata obscure source | Accountant, PDF Hunter, AIVS | P2 | __pycache__ files; .idea directories | Separate cleanup after review; do not silently delete tracked files |
| Repository topics absent | Profile, PDF Hunter, Literature Parser, AIVS | P2 | GitHub repository metadata | Suggest verified technology topics in final report |
| CV chronology, language levels and external contact details unavailable | Portfolio | P1 | No existing CV supplied; request confirms only role, skills, AIVS facts and approximately eight years running a manufacturing business | Draft verified content; mark missing fields NEEDS_USER_CONFIRMATION in report |

The commercial AIVS facts in the request are authorized owner statements: eight stages with specifications/gates/checks, deterministic extraction plus LLM reasoning, Ed25519 report attestation, evidence guardrails, 4300+ automated tests, six report languages and real paid audits. They are not measurements of the public snapshot.
