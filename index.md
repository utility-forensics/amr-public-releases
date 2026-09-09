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
| **AMR-R0010 / LR 2.2** | 2026-09-09 | AMR Console | Sliding-scale billing improvement: energy is allocated consistently across blocks, Network Surcharge uses the full eligible consumption, and monthly-bill integrity checks are stronger. |
| **AMR-R0009 / LR 2.1** | 2026-08-31 | AMR Console | Billing and Council-comparison refinement release covering modern Council Bill workflows, side-by-side audited comparisons, improved PDF/CSV output, standardized time-of-use presentation, clearer Profile statistics, reactive meter-total integrity, and corrected City Power Network Surcharge handling. |
| **AMR-R0008 / LR 2.0** | 2026-08-22 | AMR Console | Major Console release covering billing and Bills workflow improvements, Bill Wizard usability, Profile presentation, formal PDF output, Technical Pages, login/session handling, and stronger production-release safeguards. |
| **AMR-R0007** | 2026-08-05 | AMR Server | EDMI Atlas2 Profile reading reliability, interval handling, and validated energy scaling improvements. |
| **AMR-R0006** | 2026-08-03 | AMR Server | Metcom Profile totals reliability improvement for completed reads that report meter-clock warnings. |
| **AMR-R0005** | 2026-07-31 | AMR Server | Metcom Profile continuity improvement across valid meter outage/gap conditions, with stronger communications diagnostics. |
| **AMR-R0004** | 2026-07-29 | AMR Console | Comms Monitor and Profile reload improvements, including a selectable Profile start date and improved request handling. |

### LR 2.2 highlights

LR 2.2 is the current AMR Console production release. Sliding-scale energy charges now allocate the full consumption consistently across tariff blocks. Network Surcharge is calculated independently on eligible consumption, and percentage surcharges follow the reconciled charges.

Additional integrity checks prevent a monthly bill from being saved when its energy allocation cannot be reconciled. Provisional calculations remain available for review. Existing saved bills remain unchanged by this release.

Earlier releases and their full summaries remain in the [release register](releases.md).

## Notes

Detailed implementation evidence, internal validation records, exact source identities, customer-specific findings, and operational notes are kept privately by Utility Forensics.
