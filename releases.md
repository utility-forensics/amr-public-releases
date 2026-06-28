# AMR Public Release Register

This page records high-level AMR system releases and improvements for management visibility.

It is intentionally non-technical and does not include customer names, account numbers, database output, server details, internal logs, or private operational information.

---

## Release Summary

| Release | Status | System Area | Summary |
|---|---|---|---|
| AMR-R0001 | Released | AMR Server / Database | Meter reading processing performance improvement. |
| AMR-R0002 | Released | AMR Console | Comms Monitor link corrected for migrating to amr-uf-africa.co.za. |

---

## AMR-R0001 - Meter Reading Database Index

**Status:** Released  
**System area:** AMR Server / Database  
**Release type:** Performance and reliability improvement

The AMR system was experiencing slow processing when checking and handling meter reading requests. The cause was traced to database lookups on a large meter reading table that were not using an appropriate index. A database index was added so that the system can find pending meter reading requests much faster.

This improved system responsiveness and reduced delays in normal AMR processing.

---

## AMR-R0002 - Relative Comms Monitor Link

**Status:** Released  
**System area:** AMR Console  
**Release type:** Environment correctness and operational usability

The Comms Monitor link in the AMR Console used a fixed website address. This became a problem when migrating from amr.utilityforensics.co.za to amr.uf-africa.co.za

The link was changed to use a relative path, so each environment opens the correct Comms Monitor for that environment. In addition to supporting amr.uf-africa.co.za, it also supports candidate and production releases.

---

## Notes

The detailed technical evidence, private release notes, implementation details, pull requests, screenshots, SQL checks, and rollback notes are kept in private Utility Forensics repositories.

This public register is only a management-facing summary.
