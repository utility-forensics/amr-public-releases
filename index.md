---
layout: default
title: AMR System Releases
---

# AMR System Releases

This site provides a concise management-facing summary of AMR system releases and production improvements.

It intentionally excludes customer names, account numbers, meter identifiers, internal server details, database output, logs, screenshots, credentials, private technical evidence, and rollback material.

## Current Release Register

[View the AMR Public Release Register](releases.md)

## Latest Released Items

| Release | Date | System Area | Summary |
|---|---|---|---|
| **AMR-R0009 / LR 2.1** | 2026-08-31 | AMR Console | Billing and Council-comparison refinement release covering modern Council Bill workflows, side-by-side audited comparisons, improved PDF/CSV output, standardized time-of-use presentation, clearer Profile statistics, reactive meter-total integrity, and corrected City Power Network Surcharge handling. |
| **AMR-R0008 / LR 2.0** | 2026-08-22 | AMR Console | Major Console release covering billing and Bills workflow improvements, Bill Wizard usability, Profile presentation, formal PDF output, Technical Pages, login/session handling, and stronger production-release safeguards. |
| **AMR-R0007** | 2026-08-05 | AMR Server | EDMI Atlas2 Profile reading reliability, interval handling, and validated energy scaling improvements. |
| **AMR-R0006** | 2026-08-03 | AMR Server | Metcom Profile totals reliability improvement for completed reads that report meter-clock warnings. |
| **AMR-R0005** | 2026-07-31 | AMR Server | Metcom Profile continuity improvement across valid meter outage/gap conditions, with stronger communications diagnostics. |
| **AMR-R0004** | 2026-07-29 | AMR Console | Comms Monitor and Profile reload improvements, including a selectable Profile start date and improved request handling. |

### LR 2.1 highlights

LR 2.1 is the current AMR Console production release. It builds on LR 2.0 with focused improvements to billing review, Council-bill comparison and meter-total presentation:

- modernised Council Bill entry, editing and validation with current VAT handling;
- side-by-side Utility Forensics and Council Bill comparison for the same billing period;
- clear tariff MATCH / MISMATCH / UNVERIFIED status to help operators identify configuration differences;
- comparison summaries for energy, demand and financial totals, including signed percentage difference;
- improved comparison PDF output as one continuous landscape document with aligned left/right columns;
- downloadable comparison CSV output for further review and audit;
- standardised South African time-of-use terminology and order: **Peak, Standard, Off-Peak**;
- improved handling of cumulative kvarh Meter Totals so valid meter readings are preserved independently of chargeable reactive-energy rules;
- unavailable reactive reading usage now displays **N/A** rather than an invented zero;
- clearer Profile statistics for highest, average and lowest kW, kVA and power factor;
- corrected City Power Network Surcharge handling for business tariffs and residential first-500-kWh exemption/excess-only charging; and
- stronger regression, forensic package review and release verification around the affected billing paths.

LR 2.1 was fully validated through TEST, Release Candidate verification, an exhaustive package review and controlled LIVE commissioning before release acceptance.

Earlier releases and the full LR 2.1 feature summary are listed in the full register.

## Notes

Detailed implementation evidence, internal validation records, exact source identities, customer-specific findings, and operational notes are kept privately by Utility Forensics.
