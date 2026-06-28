# AMR Public Release Register

This page records high-level AMR system releases and improvements for management visibility.

It is intentionally non-technical and does not include customer names, account numbers, database output, server details, internal logs, or private operational information.

---

## Release Summary

| Release | Status | System Area | Summary |
|---|---|---|---|
| AMR-R0001 | Released | AMR Server / Database | Meter reading processing performance improvement. |
| AMR-R0002 | Candidate / Pending live confirmation | AMR Console | Comms Monitor link corrected for candidate and live environments. |

---

## AMR-R0001 - Meter Reading Database Index

**Status:** Released  
**System area:** AMR Server / Database  
**Release type:** Performance and reliability improvement

The AMR system was experiencing slow processing when checking and handling meter reading requests. The cause was traced to database lookups on a large meter reading table that were not using an appropriate index. A database index was added so that the system can find pending meter reading requests much faster.

This improved system responsiveness and reduced delays in normal AMR processing.

---

## AMR-R0002 - Relative Comms Monitor Link

**Status:** Candidate / Pending live confirmation  
**System area:** AMR Console  
**Release type:** Environment correctness and operational usability

The Comms Monitor link in the AMR Console used a fixed website address. This meant that the candidate testing system could open the production Comms Monitor instead of its own local version.

The link was changed to use a relative path, so each environment opens the correct Comms Monitor for that environment. This supports safer candidate testing and reduces the chance of accidentally mixing candidate and production operations.

---

## Notes

The detailed technical evidence, private release notes, implementation details, pull requests, screenshots, SQL checks, and rollback notes are kept in private Utility Forensics repositories.

This public register is only a management-facing summary.
