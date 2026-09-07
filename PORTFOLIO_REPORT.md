# Portfolio engineering report

Prepared on 7 September 2026. Public documentation is in English; the requested Dutch CV draft is the language-specific exception. No private repository was accessed or copied.

## 1. What was wrong

[AUDIT.md](AUDIT.md) records the pre-change findings and source paths. The critical issues were broken installation/badge Markdown, a missing CLI dependency, tax-recipe claims exceeding actual behavior, incorrect n8n paths, weak evidence links, and ambiguity between commercial AIVS and an incomplete public mapping project.

The review also found unclosed fences and misleading execution diagrams in three Accountant guides. Existing generated files and IDE/bytecode artifacts obscure several repositories.

## 2. What was changed

| Repository | Files | Purpose |
|---|---|---|
| BrysinSS | README.md | Role-first profile with AIVS as the main case; evidence and limits for each project |
| BrysinSS | AUDIT.md, PORTFOLIO_REPORT.md | Findings, provenance, checks and remaining work |
| BrysinSS | portfolio/aivs-case-study/README.md, ARCHITECTURE.md, TESTING.md, SECURITY_AND_TRACEABILITY.md | Safe commercial case study using only approved facts |
| BrysinSS | CV_REWRITE_EN.md, CV_REWRITE_NL.md | Verified CV content without invented chronology or language levels |
| ai-accountant-orchestra | README.md; docs/ARCHITECTURE.md; docs/NL_VAT_KOR_GUIDE.md; docs/QUICKSTART_PYCHARM.md | Correct commands, real examples, code-accurate architecture and explicit tax/validation boundaries |
| ai-accountant-orchestra | requirements.txt | Add the missing rich dependency; normalize the manifest from UTF-16 to UTF-8 |
| pdf-hunter-python | README.md | Five-source table, real example, explicit priority and failure behavior |
| pdf-hunter-python | src/fetch_unpaywall.py | Replace dummy contact email with optional UNPAYWALL_EMAIL configuration; encode query value; skip adapter without configuration |
| literature-parser-n8n | README.md | Correct workflow/screenshot links, setup, exact deduplication behavior and PDF Hunter handoff |
| AIVS-Declarative-Pipeline | README.md | Rename the displayed project to Declarative Business JSON-LD; distinguish it from commercial AIVS and document a verified direct mapping command |

The only executable source change is optional Unpaywall configuration. Tax calculation, recipes, workflow transformations, orchestration and existing tests are unchanged. The repository was renamed successfully to [declarative-business-jsonld](https://github.com/BrysinSS/declarative-business-jsonld); the new profile link and clone commands use that address. Historical audit labels and internal Python package names are retained.

### Validation

| Check | Result |
|---|---|
| Accountant dependency installation | Original pinned requirements plus rich installed in an isolated Python 3.12.14 environment |
| Accountant existing tests | **8 passed**; no test changes. Initial sandbox temp-directory failures were resolved by using a prepared temporary directory outside the sandboxed execution |
| Accountant load recipe | CLI imports correctly; status OK; normalized DataFrame shape 10 x 5 |
| Accountant summary recipe | Generated JSON/Markdown and NDJSON logs; actual summary values reproduced. Validation result is false while overall status is OK |
| Public JSON-LD existing test | **Collection error**: missing run_pipeline export in boundary module. Unchanged |
| Public JSON-LD direct mapper | Standard-library command completed successfully; JSON-LD artifact generated locally |
| PDF Hunter offline checks | 196 input records loaded; priority, empty results, failure isolation, optional email, query encoding, no HTTP without email and one-record mocked JSON-to-CSV path passed |
| PDF Hunter existing suite / CI | Neither exists; offline checks are not presented as an existing suite |
| n8n | JSON parsed; all 11 node references resolve; all six embedded JavaScript code nodes pass syntax compilation. Full n8n execution not performed |
| Python | All source files parsed with ast.parse |
| GitHub Actions YAML | Parsed statically; main push/PR triggers, Python 3.11, dependency install and pytest step inspected |
| Markdown | Local file links and internal anchors checked across tracked Markdown and new profile files; malformed guide fences corrected |
| Placeholder scan | No generic template markers remain in the reviewed portfolio Markdown. Existing implementation stubs in project code remain explicitly documented |

The baseline Accountant hosted CI run [19346772591](https://github.com/BrysinSS/ai-accountant-orchestra/actions/runs/19346772591) succeeded on 13 November 2025. After this update, hosted CI also **passed** for commit `52106b32b94003b95ef504f778f5d3f6743c2cca`: [run 34140230539](https://github.com/BrysinSS/ai-accountant-orchestra/actions/runs/34140230539).

### Source revisions audited

| Repository | Baseline revision |
|---|---|
| BrysinSS | 48e57c9ac401c790fe832c5288cd01df299aafb8 |
| ai-accountant-orchestra | f22e5e4d4e92579705c0ff1a562b7cabc791c41b |
| pdf-hunter-python | cfc9ac50d2dba0b0825d153d576ff316afdaf1df |
| literature-parser-n8n | 5a79f959d2e7cb18335e4a9f7b22d16b45c0d607 |
| AIVS-Declarative-Pipeline | c492dcdb4b196d053045bd4bba5beb628a52456d |

## 3. Remaining risks

- Accountant's BTW recipe neither calculates VAT nor filters the requested period. Validation does not enforce failure, and CLI status/exit-code semantics are weak. These need a separate behavioral change with meaningful integration tests.
- PDF Hunter conflates unavailable PDFs with request failures, retains DOI URL prefixes and lacks retry/backoff, detailed error logs, pinned dependencies and CI. Its live five-source batch was not run.
- n8n retains DOI URL prefixes, uses array-index topic pairing and first-record metadata, lacks pagination and has no verified runtime version. Live API access is unverified; the export's lack of credentials does not prove providers need none. See [Crossref access documentation](https://www.crossref.org/documentation/retrieve-metadata/rest-api/access-and-authentication/) and [OpenAlex access reference](https://help.openalex.org/access/).
- Public JSON-LD has broken boundary contracts, incomplete orchestration and no full dependency manifest, CI or demonstrated schema.org validator.
- Client-like files already present in the public JSON-LD repository require owner review. No file is assumed sanitized simply because it is public.
- PDF Hunter, n8n and the public JSON-LD repository have no LICENSE file; no license was invented. Existing licenses were preserved.
- This is not a security audit of repository history. Existing stub code and IDE/bytecode files were not silently removed.

## 4. Claims requiring user verification

| Item | Status |
|---|---|
| AIVS eight stages, specifications/gates/checks, deterministic extraction + LLM reasoning, Ed25519, guardrails, 4300+ tests, six languages, paid audits | Already confirmed by the owner; no repeat confirmation needed. Independently unverified private-system facts |
| Approximately eight years independently running a manufacturing business | Already confirmed by the owner |
| Public-safe stage names, detailed gate criteria and signed-payload verification procedure | NEEDS_USER_CONFIRMATION before adding |
| Exact six report languages, current test count/date/revision and sanitized test summary | NEEDS_USER_CONFIRMATION before expanding evidence |
| Sanitized commercial audit report | Completed: public AIVS sample includes JSON summaries, validated HTML derivatives, two re-rendered PDFs and a SHA-256 manifest |
| Email, LinkedIn, phone, location, work authorization, dates, business name and education | NEEDS_USER_CONFIRMATION; omitted from public claims |
| Language levels | NEEDS_USER_CONFIRMATION; no levels supplied, added or changed |
| Production readiness, measured impact, revenue, client names, coverage percentages, continuous delivery deployments | Unverified; deliberately not claimed |

## 5. Recommended next steps

1. Update any other local clones or external references to `declarative-business-jsonld`; the GitHub rename and the new portfolio links are complete.
2. Add an approved sanitized AIVS report and test-run summary. This would provide the strongest new engineering evidence.
3. Implement and test Accountant's validation gate, failure exit codes, period filtering and explicit VAT step in a separate change.
4. Normalize DOI prefixes at the research workflow boundary; add source-error diagnostics and meaningful PDF resolver tests/CI.
5. Repair public JSON-LD contracts before promoting it as a runnable pipeline. Review existing client-like data and select licenses deliberately.
6. Complete CV contact, chronology, education and language fields from confirmed facts.

Suggested repository descriptions and topics (not applied automatically):

| Repository | Description | Topics |
|---|---|---|
| ai-accountant-orchestra | YAML-driven Python transaction processing with NDJSON logs, VAT calculation functions, pytest and CI | python, automation, yaml, pytest, github-actions |
| pdf-hunter-python | Resolve open-access PDF links through official APIs and document endpoints with explicit source priority | python, api, open-access, research-automation |
| literature-parser-n8n | n8n workflow for Crossref/OpenAlex metadata collection, normalization and article export | n8n, crossref, openalex, data-pipeline |
| declarative-business-jsonld | Map declared business fields to JSON-LD with explicit Python transformations | python, json-ld, structured-data, data-mapping |

## 6. Suggested top three repositories to pin

1. **BrysinSS** — makes the commercial AIVS case study accessible as the leading engineering case without exposing its implementation.
2. **ai-accountant-orchestra** — strongest inspectable Python/test/CI evidence, with honest scope boundaries.
3. **pdf-hunter-python** — complementary API integration and deterministic selection evidence; keep its testing limitations visible.

Keep Literature Parser linked as the upstream workflow. Promote Declarative Business JSON-LD after its contracts and public-data boundaries are repaired.

## Logical delivery groups

Audit; profile README; AIVS case study; separate project documentation/configuration commits per repository; validation/report; CV drafts. Runtime logs, private data and generated local mapping output are excluded from the delivery commits.

## Publication verification

All 18 delivered files were fetched back from GitHub and matched the prepared UTF-8 content. All 17 external Markdown URLs returned HTTP 200, including the CI badge, which returned SVG showing passing. Local links and internal Markdown anchors passed across 23 reviewed documents; no unbalanced fences or generic template markers remained. GitHub rendered the AIVS eight-stage Mermaid diagram successfully.

Changes were published as separate commits, with this final verification added as a follow-up documentation commit:

| Group | Commit |
|---|---|
| Audit | acea84d6bca1eacb942bf33a121cf71ddaaaceb3 |
| Profile | 6f9099078283767d96678ee428abd3e301491062 |
| Commercial AIVS case study | 4e68da3efe12048d7b835949b2b93a5ea59c94c4 |
| Accountant docs and dependency | 52106b32b94003b95ef504f778f5d3f6743c2cca |
| PDF Hunter docs and contact configuration | 7979680ce7fe078df93d5c4d6749f7e8772fd84e |
| Literature Parser docs | 345caaa6d941d8bfe5b085dcb8e06d592299c16f |
| Declarative Business JSON-LD docs | f3fd832d7f09f6cc839e6f63fba4eecb1a3f5adf |
| Validation report | 2641db0cf7a0ebc415a368d3934253cab292b8fc |
| CV drafts | 93c3e34e51b735a19ba2a8a99ee84b46e578dd17 |
