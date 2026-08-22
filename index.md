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
| **AMR-R0008 / LR 2.0** | 2026-08-22 | AMR Console | Major Console release covering billing and Bills workflow improvements, Bill Wizard usability, Profile presentation, formal PDF output, Technical Pages, login/session handling, and stronger production-release safeguards. |
| **AMR-R0007** | 2026-08-05 | AMR Server | EDMI Atlas2 Profile reading reliability, interval handling, and validated energy scaling improvements. |
| **AMR-R0006** | 2026-08-03 | AMR Server | Metcom Profile totals reliability improvement for completed reads that report meter-clock warnings. |
| **AMR-R0005** | 2026-07-31 | AMR Server | Metcom Profile continuity improvement across valid meter outage/gap conditions, with stronger communications diagnostics. |
| **AMR-R0004** | 2026-07-29 | AMR Console | Comms Monitor and Profile reload improvements, including a selectable Profile start date and improved request handling. |
| **AMR-R0003** | 2026-07-29 | AMR Server | Profile totals integrity improvement to ensure updates remain scoped to the intended meter. |

### LR 2.0 highlights

LR 2.0 is the current major AMR Console production release. At management level, the release delivered:

- a substantially improved Bills area and Bill Wizard workflow;
- clearer billing presentation and stronger sliding-block tariff handling;
- improved Profile viewing, charting, navigation and data presentation;
- formal saved-bill PDF presentation with updated branding, layout and footer treatment;
- improved Technical Pages history, electrical-unit presentation and phasor visualisation;
- improved login/session behaviour and safer authentication handling;
- groundwork for more traceable bill-email processing while leaving customer mail disabled until separately commissioned;
- broader automated regression coverage and stronger TEST/RC/LIVE release verification; and
- a controlled LIVE maintenance mode and pre-open static-asset verification process for safer production deployments.

Earlier releases and the full LR 2.0 summary are listed in the full register.

## Notes

Detailed implementation evidence, internal validation records, exact source identities, customer-specific findings, and operational notes are kept privately by Utility Forensics.
