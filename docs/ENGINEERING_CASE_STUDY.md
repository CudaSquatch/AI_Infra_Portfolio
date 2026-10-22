# Engineering Case Study — From GPU Thermal Evidence to Corrective Learning

**AI_Infra v0.2 · Controlled synthetic scenario**

## Problem

A dashboard can flag an abnormal GPU temperature without explaining why it was flagged, who owns the response, what readiness milestone it affects, or whether a trialed response was effective. Infrastructure reliability depends on connecting those steps with evidence.

## Scenario and sequence

A reproducible **GPU thermal degradation** scenario models GPU-01 temperature rising while effective utilization decreases and power increases. The environment contains 12 hosts, 8 GPUs and 3 zones. Scenario ground truth is retained separately from the measurements and does **not** constitute a diagnosed physical fault.

1. **Observe.** Capture labeled telemetry by asset, metric, timestamp and origin.
2. **Detect.** Evaluate thresholds and other configured signals; preserve sample IDs, measurements and thresholds.
3. **Triage.** Review incident evidence, acknowledge it, assign an owner and an action, record investigation notes.
4. **Assess readiness.** Associate an incident with a program milestone or equipment acceptance condition; review mitigation and dependencies.
5. **Investigate.** Create a persistent trouble report with containment, Five Whys, alternatives and cited evidence.
6. **Trial and review.** Record a versioned standard-work procedure, retain what was actually trialed, and enter a human-reviewed outcome with limitations.
7. **Control and communicate.** Use DMAIC stage evidence and CTQ metrics, exploratory control charts and provenance-aware reports.

![GPU telemetry history](../assets/screenshots/03-gpu-evidence.png)

![Trouble investigation with trial evidence](../assets/screenshots/08-trouble-investigation.png)

## Engineering decisions and tradeoffs

| Decision | Reason | Limitation |
| --- | --- | --- |
| Deterministic failure simulation | Repeatable demonstrations without field hardware | Not physical fault-prediction evidence |
| Three-project modular monolith | Transactional workflows with manageable deployment | Not validated for large multitenant fleets |
| Source/provenance labeling | Separate synthetic and measured contexts | Hardware collection must be proven separately |
| Preserved alert evidence | Makes incident response inspectable | Does not establish physical root cause |
| Versioned solution trials | Keeps reviewed records tied to the tested procedure | Human outcomes are not independently verified repairs |
| Statistical checks before ML | Transparent assumptions and testability | Workload effects/autocorrelation limit interpretation |

## Evidence and outcomes

The October 20, 2026 v0.2 validation record reports **31 unit tests, 14 integration/API tests, 20 published-app browser checks and 9 native Docker Compose smoke checks passed** on the documented CI environments.

This establishes a tested software workflow in a controlled setting. It does not demonstrate measured savings, uptime improvements, customer adoption, production scalability or true hardware repair effectiveness.

## Further work

Validate real read-only exporters, Windows deployment, backup/recovery and HTTPS; observe source quality and alert accuracy; strengthen identity lifecycle, independent reviewer controls and long-running performance evidence.

[Home](../README.md) · [Validation](VALIDATION.md) · [Architecture](ARCHITECTURE.md)
