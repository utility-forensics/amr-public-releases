# AMR Public Release Register

<style>
  .amr-note {
    background: #f6fbff;
    border-left: 5px solid #8fd3ff;
    padding: 12px 16px;
    margin: 16px 0;
    border-radius: 6px;
  }

  .amr-summary-table {
    width: 100%;
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
  }

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
This page records high-level AMR system releases and improvements for management visibility.
<br><br>
It is intentionally non-technical and does not include customer names, account numbers, database output, server details, internal logs, or private operational information.
</div>

---

## Release Summary

<table class="amr-summary-table">
  <thead>
    <tr>
      <th>Release</th>
      <th>Status</th>
      <th>System Area</th>
      <th>Summary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>AMR-R0001</strong></td>
      <td><span class="amr-status">Released</span></td>
      <td>AMR Server / Database</td>
      <td>Meter reading processing performance improvement.</td>
    </tr>
    <tr>
      <td><strong>AMR-R0002</strong></td>
      <td><span class="amr-status">Released</span></td>
      <td>AMR Console</td>
      <td>Comms Monitor link corrected for migrating to amr.uf-africa.co.za.</td>
    </tr>
  </tbody>
</table>

---

<h2 class="amr-release-heading">AMR-R0001 - Meter Reading Database Index</h2>

**Status:** <span class="amr-status">Released</span>  
**System area:** AMR Server / Database  
**Release type:** Performance and reliability improvement

The AMR system was experiencing slow processing when checking and handling meter reading requests. The cause was traced to database lookups on a large meter reading table that were not using an appropriate index. A database index was added so that the system can find pending meter reading requests much faster.

This improved system responsiveness and reduced delays in normal AMR processing.

---

<h2 class="amr-release-heading">AMR-R0002 - Relative Comms Monitor Link</h2>

**Status:** <span class="amr-status">Released</span>  
**System area:** AMR Console  
**Release type:** Environment correctness and operational usability

The Comms Monitor link in the AMR Console used a fixed website address. This became a problem when migrating from amr.utilityforensics.co.za to amr.uf-africa.co.za.

The link was changed to use a relative path, so each environment opens the correct Comms Monitor for that environment. In addition to supporting amr.uf-africa.co.za, it also supports candidate and production releases.

---

## Notes

The detailed technical evidence, private release notes, implementation details, pull requests, screenshots, SQL checks, and rollback notes are kept in private Utility Forensics repositories.

This public register is only a management-facing summary.
