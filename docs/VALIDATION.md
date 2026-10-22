# Testing and Validation

**Validation record:** v0.2, October 20, 2026, from the separately maintained private engineering implementation. This portfolio summarizes recorded results; rebuilding the portfolio does not rerun the application test suites.

## Native CI evidence

The documented successful GitHub Actions run tested application commit `40016fb44977ac9c380fdac6e0a5cfb805cb0cd1` using a Linux runner and native PostgreSQL 17.11-alpine, followed by a Release build/publish and Docker Compose smoke tests.

| Check | Recorded result |
| --- | --- |
| .NET Release build | Passed with 0 errors and 0 warnings |
| Unit tests | **31 passed**; 0 failed or skipped |
| Integration/API tests | **14 passed**; 0 failed or skipped |
| Browser checks on published application | **20 passed** |
| Native Docker Compose smoke checks | **9 passed** |
| Known dependency vulnerability audit | Passed in documented run |
| Project-specific secrets-pattern scan | 0 findings in documented run |

Browser checks included published JavaScript delivery, authentication, changing simulated telemetry, history, thermal failure detection, preserved incident evidence, owner/actions, program risk, Five Whys, versioned solution trial/review, DMAIC, exploratory SPC, report exports and demo-mode safeguards.

An actual integration issue was found during verification: normal pages could render while the production Blazor framework script was missing. The release fixed asset delivery and added published-browser regression checks, rather than treating a successful page response as proof of interactive functionality.

## Interpret results precisely

These results substantiate the listed **software behaviors in controlled synthetic environments**. They do not prove real GPU compatibility, operational uptime, physical fault-prediction performance, multi-fleet throughput, financial savings or production security.

A separate sequential PostgreSQL WebAssembly harness recorded limited synthetic ingestion performance; it is **not** a native database benchmark or validated scaling claim.

## Not yet verified

- Startup, configuration and persisted operations on the intended Windows machine.
- Backup restoration, restart recovery and HTTPS/proxy deployment.
- At least one real read-only host/GPU exporter with accurate freshness and identity attribution.
- Sustained real-source ingestion, retention/rollup performance and false-positive rates.
- Production identity lifecycle, separate approver controls and full threat/security review.

[Overview](../README.md) · [Status and future validation](PROJECT_STATUS.md)
