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
  .amr-summary-table th:nth-child(1), .amr-summary-table td:nth-child(1) { width: 13%; }
  .amr-summary-table th:nth-child(2), .amr-summary-table td:nth-child(2) { width: 12%; }
  .amr-summary-table th:nth-child(3), .amr-summary-table td:nth-child(3) { width: 12%; }
  .amr-summary-table th:nth-child(4), .amr-summary-table td:nth-child(4) { width: 18%; }
  .amr-summary-table th:nth-child(5), .amr-summary-table td:nth-child(5) { width: 45%; }
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
    <tr><th>Release</th><th>Release Date</th><th>Status</th><th>System Area</th><th>Summary</th></tr>
  </thead>
  <tbody>
    <tr><td><strong>AMR-R0010 / LR 2.2</strong></td><td>2026-09-09</td><td><span class="amr-status">Released</span></td><td>AMR Console</td><td>Sliding-scale billing improvement: energy is allocated consistently across blocks, Network Surcharge uses the full eligible consumption, and monthly-bill integrity checks are stronger.</td></tr>
    <tr><td><strong>AMR-R0009 / LR 2.1</strong></td><td>2026-08-31</td><td><span class="amr-status">Released</span></td><td>AMR Console</td><td>Billing and Council-comparison refinement release covering modern Council Bill workflows, audited side-by-side comparisons, improved PDF/CSV output, standardized time-of-use presentation, clearer Profile statistics, reactive meter-total integrity, and corrected Network Surcharge handling.</td></tr>
    <tr><td><strong>AMR-R0008 / LR 2.0</strong></td><td>2026-08-22</td><td><span class="amr-status">Released</span></td><td>AMR Console</td><td>Major Console release covering billing and Bills workflows, Bill Wizard usability, Profile presentation, formal PDF output, Technical Pages, login/session handling, and stronger release safeguards.</td></tr>
    <tr><td><strong>AMR-R0007</strong></td><td>2026-08-05</td><td><span class="amr-status">Released</span></td><td>AMR Server</td><td>EDMI Atlas2 Profile reading reliability, interval handling, and validated energy scaling improvements.</td></tr>
    <tr><td><strong>AMR-R0006</strong></td><td>2026-08-03</td><td><span class="amr-status">Released</span></td><td>AMR Server</td><td>Metcom Profile totals reliability improvement for completed reads that report meter-clock warnings.</td></tr>
    <tr><td><strong>AMR-R0005</strong></td><td>2026-07-31</td><td><span class="amr-status">Released</span></td><td>AMR Server</td><td>Metcom Profile continuity improvement across valid meter outage/gap conditions, with stronger communications diagnostics.</td></tr>
    <tr><td><strong>AMR-R0004</strong></td><td>2026-07-29</td><td><span class="amr-status">Released</span></td><td>AMR Console</td><td>Comms Monitor and Profile reload improvements, including a selectable Profile start date and improved request handling.</td></tr>
    <tr><td><strong>AMR-R0003</strong></td><td>2026-07-29</td><td><span class="amr-status">Released</span></td><td>AMR Server</td><td>Profile totals integrity improvement to ensure updates remain scoped to the intended meter.</td></tr>
    <tr><td><strong>AMR-R0002</strong></td><td>2026-06-28</td><td><span class="amr-status">Released</span></td><td>AMR Console</td><td>Comms Monitor link corrected for the current candidate and production environments.</td></tr>
    <tr><td><strong>AMR-R0001</strong></td><td>2026-06-28</td><td><span class="amr-status">Released</span></td><td>AMR Server / Database</td><td>Meter reading processing performance improvement.</td></tr>
  </tbody>
</table>

---

<h2 class="amr-release-heading">AMR-R0010 / LR 2.2 - Sliding-Scale Billing Integrity</h2>

**Status:** <span class="amr-status">Released</span><br>
**System area:** AMR Console<br>
**Release type:** Focused billing correctness and integrity improvement<br>
**Release date:** 2026-09-09

LR 2.2 improves sliding-scale billing so energy is allocated consistently across tariff blocks. Network Surcharge uses the full eligible consumption independently, and percentage surcharges follow the reconciled charges. This improves agreement between energy quantities and the resulting bill totals.

Additional integrity checks prevent a monthly bill from being saved when its energy allocation cannot be reconciled, while provisional calculations remain available for review. The release preserves existing saved bills; any operational correction of an earlier bill remains a separate authorised action.

---

<h2 class="amr-release-heading">AMR-R0009 / LR 2.1 - Billing and Council Comparison Refinement</h2>

**Status:** <span class="amr-status">Released</span>  
**System area:** AMR Console  
**Release type:** Billing review, comparison, presentation and tariff-handling improvement  
**Release date:** 2026-08-31

LR 2.1 is a focused follow-up to LR 2.0. It improves how Council electricity bills are entered, reviewed and compared with Utility Forensics calculations, while also improving Profile statistics, meter-total presentation and Network Surcharge handling.

### Council Bill workflow

- Modernised Council Bill entry, editing and validation.
- Standardised new and edited Council Bill VAT handling at the current 15% rate while preserving historical stored VAT when older bills are viewed.
- Improved the grouping and presentation of Council Bill charge categories.
- Added stronger validation so incomplete or inconsistent draft bill information is identified before use.

### Utility Forensics vs Council Bill comparison

- Added a modern side-by-side comparison between the Council Bill and a fresh Utility Forensics recalculation for the same account, billing period and Council tariff.
- Added clear tariff verification states: **MATCH**, **MISMATCH** and **UNVERIFIED**.
- Presents the Utility Forensics and Council values in parallel for easier operator and management review.
- Shows signed differences so over- and under-positions are clear rather than being reduced to absolute values.
- Aligns the left and right comparison columns for **Description, Units, Rate and Amount** to make detailed comparisons easier to read.
- Keeps factual differences visible when one side contains a charge that is absent on the other side.

### Comparison summary and export

- Added a Bill Comparison Summary covering the principal energy, demand and financial totals.
- Shows Utility Forensics, Council and Difference values in a compact management-friendly format.
- Includes signed percentage difference for the financial comparison.
- Added an 11-column CSV export so comparison results can be reviewed further in spreadsheet or audit workflows.

### Comparison PDF output

- Reworked the comparison PDF into a continuous landscape presentation rather than separate or awkwardly paginated bill panels.
- Uses a balanced Utility Forensics / Council layout with consistent internal column widths.
- Improved wrapping and alignment so long descriptions do not disturb the Units, Rate or Amount columns.
- Keeps the comparison summary and difference information together with the detailed bill comparison.

### Time-of-use terminology and ordering

- Standardised South African time-of-use terminology to **Peak, Standard, Off-Peak**.
- Replaced the legacy presentation term **Shoulder** with **Standard** where it represented the same middle time-of-use band.
- Standardised categorical bill presentation order to **Peak → Standard → Off-Peak**.
- Preserved chronological ordering on time-based Profile graphs, where clock sequence remains more appropriate than categorical tariff order.

### Meter Totals and reactive-energy presentation

- Improved cumulative kvarh Meter Totals so valid start and end meter readings are preserved independently of the separate rule used to calculate chargeable reactive energy.
- Unavailable cumulative reactive readings are now treated as unavailable rather than being replaced with artificial zero values.
- Corrected Council Comparison usage presentation so missing reactive boundaries display derived usage as **N/A**, never an invented **0.000**.
- Valid kWh and kvarh boundary differences continue to be calculated and displayed normally.

### Profile statistics

- Modernised the Profile **Stats on kW, kVA & PF** presentation.
- Presents highest, average and lowest values in a clearer card layout.
- Improves visual distinction between kW, kVA and power factor while retaining the established underlying statistics.

### Network Surcharge handling

- Corrected City Power Network Surcharge treatment for the affected business tariffs so applicable business consumption is charged according to the configured surcharge rate rather than being incorrectly gated by a residential-style threshold.
- Corrected residential Network Surcharge handling so the first 500 kWh remains exempt and only consumption above 500 kWh is allocated to the surcharge.
- Preserved the separate existing percentage-surcharge relationships and did not alter unrelated tariff rates, saved bills or Council Bill records.
- The change is implemented through a generic excess-above-threshold rule rather than customer-specific billing logic.

### Reliability and release assurance

- Added focused automated coverage for Council Bill modernisation, comparison PDF lifecycle, time-of-use presentation, reactive Meter Totals and Network Surcharge behaviour.
- The final LR 2.1 package received a full source-to-feature provenance review before release, including all production changes and shared AMR/KT paths.
- A pre-release review identified and corrected the missing-reactive-boundary presentation issue before LIVE deployment.
- The exact accepted production package then passed final Release Candidate validation and controlled LIVE commissioning before release acceptance.

### Management outcome

LR 2.1 makes Council-bill auditing substantially easier to understand and present. Operators can compare Council and Utility Forensics results side by side, export the comparison, generate a cleaner customer-facing PDF, use standard South African TOU terminology, and rely on improved reactive Meter Totals and Network Surcharge treatment. The release is intentionally focused: separate Bill Import, deeper kVA/PF/kvarh forensic work and historical reread/recovery work are not part of LR 2.1.

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
