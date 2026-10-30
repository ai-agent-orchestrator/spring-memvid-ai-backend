# Architecture Evidence Plan

**Status: NOT_RUN. No measurements or passing reports are attached.**

## Reproducible records

Record the code commit; policy, schema, SDK, and model versions; OS and resources; dataset version; execution time; expected and observed outcomes; limitations; and reproduction commands. Use synthetic data and minimal identifiers. Do not publish client content or credentials.

| ID | Claim | Method | Evidence to record |
|---|---|---|---|
| ISO-01 | Case boundaries hold | Attempt cross-tenant and unassigned-case access | Denials, file-open attempts, returned sources |
| ISO-02 | Bypass paths are blocked | Direct Python requests, forged/expired tokens, traversal and symlinks | Identity checks and rejection before file access |
| ISO-03 | Secondary storage respects scope | Test caches, temporary plaintext, backups and revoked access | Disclosure or reappearance after deletion/revocation |
| BUD-01 | Reservations are atomic | Concurrent requests near the budget limit; duplicate IDs | Approved total, open balance, duplicate paid calls |
| BUD-02 | Runtime limits hold | Exceed steps, retries, models, output and deadlines | Allowed/actual stages, rejected calls, cancellation timing |
| BILL-01 | Spending is traceable | Inject timeout, cancellation, missing usage and invalid JSON | Reserved, actual, estimated and unresolved costs; provider differences |
| QUAL-01 | Evidence quality is measurable | Fixed Korean synthetic cases with predefined source IDs | Recall@k, wrong sources, missing numbers, negation and contradictions |
| HITL-01 | Review resumption is authorized | Revoke access, change drafts/sources, restart while waiting | Revalidation, re-reservation and stale-draft handling |
| COST-01 | Operational footprint improves | Compare matched data, workload and retention | Compute, storage, backups, models, embeddings, maintenance time and total cost |
| REC-01 | Memory can recover | Interrupted writes, locks, reopen and encrypted-backup restoration | Missing/duplicate data, retrieval consistency and recovery time |

## Interpretation rules

- Report only the tested scope, data and versions. Finite tests cannot rule out every possible breach.
- Separate retrieval from end-to-end latency; include p50/p95, workload and resources.
- Do not infer superiority by comparing a private backend with a public chat interface. Match product, version, configuration, permissions and scope.
- Distinguish lower search-database charges from lower total operating cost. Include all consumed resources.
- Retain failed tests and unresolved provider costs in the report.

## Result template

```text
Test ID:
Status: NOT_RUN / PASS / FAIL / INCONCLUSIVE
Code commit and policy / SDK / model versions:
Dataset, environment and execution time:
Reproduction steps:
Expected outcome:
Observed outcome and sanitized evidence location:
Limitations and unresolved items:
```

Attach sanitized logs, evaluation tables and cost reconciliation when available, and link them to the corresponding claims in the main README.
