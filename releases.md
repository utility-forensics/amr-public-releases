---
layout: default
title: AMR Public Release Register
---

<h1 class="amr-page-title">AMR Public Release Register</h1>

<style>
  .amr-page-title {
    color: #176b98;
    background: #bfe4f8;
    padding: 12px 16px;
    border-left: 7px solid #176b98;
    border-radius: 6px;
    font-size: 2em;
    font-weight: 600;
  }
  .amr-note {
    background: #f6fbff;
    border-left: 5px solid #8fd3ff;
    padding: 12px 16px;
    margin: 16px 0;
    border-radius: 6px;
  }
  .amr-summary-table {
    display: table !important;
    width: 100% !important;
    max-width: 100% !important;
    min-width: 100% !important;
    table-layout: fixed;
    border-collapse: collapse;
    margin: 18px 0 28px 0;
  }
  .amr-summary-table th {
    background: #d9f0ff;
    border: 1px solid #b9dff5;
    padding: 10px;
    text-align: left;
  }
  .amr-summary-table td {
    background: #e7f8e7;
    border: 1px solid #c9e8c9;
    padding: 10px;
    vertical-align: top;
    word-wrap: break-word;
  }
  .amr-summary-table th:nth-child(1), .amr-summary-table td:nth-child(1) { width: 14%; }
  .amr-summary-table th:nth-child(2), .amr-summary-table td:nth-child(2) { width: 14%; }
  .amr-summary-table th:nth-child(3), .amr-summary-table td:nth-child(3) { width: 22%; }
  .amr-summary-table th:nth-child(4), .amr-summary-table td:nth-child(4) { width: 50%; }
  .amr-release-heading {
    color: #2b8fc6;
    background: #d9f0ff;
    padding: 10px 14px;
    border-left: 6px solid #2b8fc6;
    border-radius: 6px;
    margin-top: 28px;
  }
  .amr-status {
    display: inline-block;
    background: #e7f8e7;
    border: 1px solid #9bd49b;
    border-radius: 999px;
    padding: 3px 10px;
    font-weight: 600;
  }
</style>

<div class="amr-note">
This page records high-level AMR system releases and production improvements for management visibility.
<br><br>
It is intentionally non-technical and does not include customer names, account numbers, meter identifiers, database output, server details, internal logs, credentials, screenshots, or private operational evidence.
</div>

---

## Release Summary

<table class="amr-summary-table">
  <thead>
    <tr><th>Release</th><th>Status</th><th>System Area</th><th>Summary</th></tr>
  </thead>
  <tbody>
    <tr><td><strong>AMR-R0008 / LR 2.0</strong></td><td><span class="amr-status">Released</span></td><td>AMR Console</td><td>Major Console release covering billing and Bills workflows, Bill Wizard usability, Profile presentation, formal PDF output, Technical Pages, login/session handling, and stronger release safeguards.</td></tr>
    <tr><td><strong>AMR-R0007</strong></td><td><span class="amr-status">Released</span></td><td>AMR Server</td><td>EDMI Atlas2 Profile reading reliability, interval handling, and validated energy scaling improvements.</td></tr>
    <tr><td><strong>AMR-R0006</strong></td><td><span class="amr-status">Released</span></td><td>AMR Server</td><td>Metcom Profile totals reliability improvement for completed reads that report meter-clock warnings.</td></tr>
    <tr><td><strong>AMR-R0005</strong></td><td><span class="amr-status">Released</span></td><td>AMR Server</td><td>Metcom Profile continuity improvement across valid meter outage/gap conditions, with stronger communications diagnostics.</td></tr>
    <tr><td><strong>AMR-R0004</strong></td><td><span class="amr-status">Released</span></td><td>AMR Console</td><td>Comms Monitor and Profile reload improvements, including a selectable Profile start date and improved request handling.</td></tr>
    <tr><td><strong>AMR-R0003</strong></td><td><span class="amr-status">Released</span></td><td>AMR Server</td><td>Profile totals integrity improvement to ensure updates remain scoped to the intended meter.</td></tr>
    <tr><td><strong>AMR-R0002</strong></td><td><span class="amr-status">Released</span></td><td>AMR Console</td><td>Comms Monitor link corrected for the current candidate and production environments.</td></tr>
    <tr><td><strong>AMR-R0001</strong></td><td><span class="amr-status">Released</span></td><td>AMR Server / Database</td><td>Meter reading processing performance improvement.</td></tr>
  </tbody>
</table>

---

<h2 class="amr-release-heading">AMR-R0008 / LR 2.0 - Major AMR Console Release</h2>

**Status:** <span class="amr-status">Released</span>  
**System area:** AMR Console  
**Release type:** Major application, usability, reliability and release-control improvement  
**Release date:** 2026-08-22

LR 2.0 is a substantial AMR Console production release focused on improving day-to-day operator workflows, billing and Profile presentation, formal customer-facing output, and the reliability of production releases.

### Billing and Bills

- Improved the Bills area so historic and current bills are easier to review.
- Improved Bill Wizard usability, including clearer account/date selection and more responsive loading behaviour.
- Improved bill presentation and handling of saved bills.
- Strengthened sliding-block tariff calculation behaviour and added regression protection around the corrected calculation paths.
- Improved the consistency between Billing views, bill preparation and saved-bill presentation.

### Profiles and meter information

- Improved Profile viewing and chart presentation, including better handling of chart data and Profile display dependencies.
- Improved Technical Pages history so operators can select and review more than only the most recent technical snapshot.
- Improved electrical-unit presentation in Technical Pages, including clear current, voltage and angle units.
- Improved phasor visualisation and tooltip presentation.

### Formal PDF presentation

- Improved formal bill PDF presentation, including Utility Forensics branding, borders, spacing and footer layout.
- Improved consistency between the on-screen saved-bill view and the formal PDF output.
- Improved multi-bill preparation so operator review and PDF generation are more predictable.

### Login, session and operational usability

- Improved login and session handling while retaining compatibility with the existing AMR Console.
- Added safer session-support foundations for future operational improvements.
- Improved Administrator loading feedback for larger meter lists.
- Removed several sources of unnecessary page jumping and presentation inconsistency in operator workflows.

### Email and traceability groundwork

- Added the application groundwork for more traceable bill-email processing and safer future mail commissioning.
- Customer email delivery remains disabled until separately commissioned and approved; LR 2.0 did not activate unattended customer mail.

### Reliability and release safeguards

- Expanded automated regression coverage across billing, Bills, Profiles, PDF presentation, Technical Pages, login/session and supporting workflows.
- Introduced clearer TEST and Release Candidate validation boundaries and required a second RC verification of the exact production merge before LIVE deployment.
- Added a controlled LIVE Maintenance Mode that blocks public application access during deployment while allowing safe origin validation.
- Added public static-asset integrity checks before reopening the application, including protection against stale CDN assets after a release.
- Improved rollback preparation and release evidence so production changes can be verified against exact accepted source and runtime state.

### Management outcome

The result is a more usable and more predictable AMR Console for operators, with stronger billing and Profile presentation, improved formal customer-facing documents, and a substantially more controlled production release process. The exact LR 2.0 production package passed TEST, two RC acceptance stages, controlled LIVE deployment and final browser/PDF acceptance before being declared released.

---

<h2 class="amr-release-heading">AMR-R0007 - EDMI Atlas2 Profile Reliability</h2>

**Status:** <span class="amr-status">Released</span>  
**System area:** AMR Server  
**Release type:** Meter protocol reliability and data-quality improvement  
**Release date:** 2026-08-05

The AMR Server's EDMI Atlas2 Profile handling was improved to make interval selection and continued Profile reading more reliable. The release includes validated energy scaling, whole-second timestamp handling, and improved continuation when reading the next available interval.

These changes improve reliable collection of Atlas2 interval data without changing Atlas1 behaviour, billing logic, or meter configuration.

---

<h2 class="amr-release-heading">AMR-R0006 - Metcom Clock/Total Recalculation Reliability</h2>

**Status:** <span class="amr-status">Released</span>  
**System area:** AMR Server  
**Release type:** Meter data-processing reliability improvement  
**Release date:** 2026-08-03

Metcom Profile processing was improved so that a successfully completed read can still recalculate interval totals when the meter reports a clock warning. The system keeps the warning visible while allowing valid completed Profile data to proceed through the normal calculation path.

The change improves recovery of correct totals from valid meter reads while retaining the existing safety checks for incomplete or uncertain reads.

---

<h2 class="amr-release-heading">AMR-R0005 - Metcom Profile Continuity Across Meter Gaps</h2>

**Status:** <span class="amr-status">Released</span>  
**System area:** AMR Server  
**Release type:** Profile reading reliability and diagnostics improvement  
**Release date:** 2026-07-31

Metcom Profile reading was improved to continue correctly across valid meter outage or no-data windows instead of treating every such response as a generic communications failure. When Profile data resumes, the normal calculation sequence continues from actual meter data without creating artificial intervals.

The same release also improved safe communications diagnostics for troubleshooting while keeping sensitive meter information protected.

---

<h2 class="amr-release-heading">AMR-R0004 - Comms Monitor and Profile Reload Improvements</h2>

**Status:** <span class="amr-status">Released</span>  
**System area:** AMR Console  
**Release type:** Operational usability and meter-support improvement  
**Release date:** 2026-07-29

The AMR Console Comms Monitor was modernised and its Profile reload workflow improved. Operators can specify the Profile start date for a controlled reload, while request handling was aligned with the normal AMR priority queue.

This provides better visibility and control when investigating or recovering meter Profile data.

---

<h2 class="amr-release-heading">AMR-R0003 - Profile Totals Integrity</h2>

**Status:** <span class="amr-status">Released</span>  
**System area:** AMR Server  
**Release type:** Data integrity and reliability improvement  
**Release date:** 2026-07-29

Profile totals updates were tightened so that an update is explicitly scoped to the intended meter and interval. This prevents an identifier shared by different meters from allowing one meter's totals update to affect another meter.

The improvement strengthens the integrity of Profile totals processing without changing the underlying totals calculation method.

---

<h2 class="amr-release-heading">AMR-R0002 - Relative Comms Monitor Link</h2>

**Status:** <span class="amr-status">Released</span>  
**System area:** AMR Console  
**Release type:** Environment correctness and operational usability  
**Release date:** 2026-06-28

The Comms Monitor link in the AMR Console used a fixed website address. This became a problem when migrating to the current production address.

The link was changed to use a relative path, so each environment opens the correct Comms Monitor for that environment. This supports both candidate and production releases.

---

<h2 class="amr-release-heading">AMR-R0001 - Meter Reading Database Index</h2>

**Status:** <span class="amr-status">Released</span>  
**System area:** AMR Server / Database  
**Release type:** Performance and reliability improvement  
**Release date:** 2026-06-28

The AMR system was experiencing slow processing when checking and handling meter reading requests. The cause was traced to database lookups on a large meter reading table that were not using an appropriate index. A database index was added so that the system can find pending meter reading requests much faster.

This improved system responsiveness and reduced delays in normal AMR processing.

---

## Notes

The detailed technical evidence, private release notes, exact source identities, implementation details, validation logs, screenshots, SQL checks, and rollback notes are kept in private Utility Forensics repositories.

This register is a management-facing release history only.
