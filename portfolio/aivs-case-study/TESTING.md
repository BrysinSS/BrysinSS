# AIVS testing and evidence

## Current suite result

The private repository was tested at commit `3809ab6ca006d397d58d65d3ea32927a3e0160e1` on 7 September 2026 with Python 3.14 and pytest 9.0.2 on Windows.

```text
python -m pytest -q -p no:cacheprovider
4308 passed, 12 skipped in 105.34s (0:01:45)
```

Collection reported exactly 4,320 tests. The completed run therefore recorded:

| Outcome | Count |
|---|---:|
| Collected | 4,320 |
| Passed | 4,308 |
| Skipped | 12 |
| Xfailed | 0 |
| Failed | 0 |
| Errors | 0 |

No coverage percentage was measured, so none is claimed.

## What the suite exercises

The collected tests span the staged audit pipeline and wrapper, including crawl and extraction behavior, structured schemas, strict-mode orchestration, model-measurement contracts, claim verification, Ed25519 attestation behavior, multilingual rendering, Stage H validation, report generation, run manifests and delivery policy.

This is a test-run result for the private AIVS repository. It is separate from the public Declarative Business JSON-LD repository and from the production audit's 108 model responses.

## Execution note

Two preliminary sandboxed runs were invalid because pytest could not keep access to its temporary root; their resulting setup errors do not describe product behavior. The reported result above is the subsequent unrestricted local run, which used the same repository commit and command and completed without failures or setup errors. Details are retained in [follow-up notes](FOLLOW_UP.md).
