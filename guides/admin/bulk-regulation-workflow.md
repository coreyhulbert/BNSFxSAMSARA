---
title: Bulk Regulation Workflow
meta: Prepared for BNSF by Corey Hulbert — Samsara Resident Consultant
summary: Bulk-change vehicles to Unregulated via CSV upload — the quick-reference version.
raw: true
---
<p>You can bulk change your vehicles' regulation mode to Unregulated using Samsara's CSV upload for gateways/vehicles. Here's the workflow:</p>
    <h3>Steps</h3>
    <ol>
      <li>Go to Settings → Devices → Vehicles (or Gateways, if that's how they're managed).</li>
      <li>Click More Actions → Download CSV to export your current vehicles/gateways with all editable fields.</li>
      <li>Open the CSV and locate the <strong>Vehicle Regulation Mode</strong> column.</li>
      <li>For every row you want changed, set that column to <strong>Unregulated</strong>. (Valid values: Regulated, Unregulated, or Mixed-Use. Leave other columns as-is — do not blank them.)</li>
      <li>Save the CSV.</li>
      <li>Back in the dashboard, choose More Actions → Upload CSV and select your edited file.</li>
      <li>Review the Preview Changes screen carefully, then Confirm to apply.</li>
    </ol>
    <h3>Notes</h3>
    <ul>
      <li><strong>Unregulated (non-CMV)</strong> removes the vehicle from ELD tracking — drivers of those vehicles will no longer be logged under HOS rules while operating them. Only apply this to vehicles genuinely not subject to the ELD mandate.</li>
      <li>If a vehicle sometimes tows a trailer that pushes it over 10,001 lb combined, use <strong>Mixed-Use</strong> instead, so the driver can toggle regulated/unregulated from the Driver App.</li>
      <li>You need Organization Administrator (or a custom admin role with Vehicles + tag edit permissions) to upload the CSV.</li>
      <li>Reference: Regulated and Unregulated Vehicles (non-CMV), and Edit Gateways in Bulk.</li>
    </ul>