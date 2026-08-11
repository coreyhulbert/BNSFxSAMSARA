---
title: Gateway Regulation Mode CSV Update Guide
meta: Created for BNSF by Corey Hulbert — Samsara Resident Consultant
summary: The full step-by-step CSV bulk-edit flow, including attribute sync and column reference.
raw: true
---
<p>A step-by-step guide to bulk-updating gateway records in the Samsara dashboard, including how to mark vehicles Regulated or Unregulated.</p>
    <h3>Choosing the right upload flow</h3>
    <p><strong>For vehicles with gateways (VGs):</strong> use Settings → Devices → Gateways → More Actions → Upload CSV → Download Devices List. This bulk-edit flow supports:</p>
    <ul>
      <li><strong>Name</strong> — update the unit number/name.</li>
      <li><strong>Vehicle Regulation Mode</strong> — valid values are Regulated or Unregulated.</li>
      <li><strong>Asset Attribute: (Attribute Name)</strong> columns — for changing asset attributes.</li>
    </ul>
    <p><strong>For non-vehicle assets</strong> (trailers, equipment, unpowered or uncategorized assets) where you only need to change the unit number/name and an attribute, use Fleet → Assets → CSV upload instead. Regulated/Unregulated is only surfaced in the gateway bulk-edit flow, not the general asset CSV.</p>
    <h3>A few important rules</h3>
    <ul>
      <li>The CSV must use the provided template and include the header row.</li>
      <li>Gateway bulk-edit files can contain up to 500 rows per upload — updates beyond that need multiple files.</li>
      <li><strong>ID</strong> and <strong>Gateway Serial</strong> are not editable — use them to match records, but don't change them.</li>
      <li>For attribute changes, the column must use an existing attribute name and valid existing value(s). Separate multiple values with semicolons; use NULL to clear the attribute. If the attribute or value doesn't exist yet, create or edit it first in Settings → Tags &amp; Attributes → Attributes.</li>
    </ul>
    <h3>Step-by-step instructions</h3>
    <ol>
      <li>Go to the Samsara dashboard and click the Settings icon at the bottom of the Fleet menu.</li>
      <li>Go to Devices → Gateways.</li>
      <li>Click More Actions → Upload CSV.</li>
      <li>Click Download Devices List — this gives you the correct template with current gateway and vehicle data.</li>
      <li>Open the file in Excel or Google Sheets and keep only the rows you want to update. The gateway CSV can contain no more than 500 rows total, including the header.</li>
      <li>In the CSV, find the Vehicle Regulation Mode column. For each row you want to change, enter either Regulated or Unregulated.</li>
      <li>Do not change the ID or Gateway Serial columns — those are identifiers and are not editable.</li>
      <li>If also updating the unit number, edit the Name column.</li>
      <li>If also updating an attribute — for this BNSF update, set <strong>Asset Attribute: CMV</strong> to <strong>CMV</strong> for every row marked Regulated, so the attribute stays in sync with the regulation mode.</li>
      <li>Save the file as a properly formatted CSV, keeping the header row intact. Use only the provided template.</li>
      <li>Go back to Settings → Devices → Gateways → More Actions → Upload CSV and choose Upload a file.</li>
      <li>Select your edited CSV, or drag and drop it into the upload window.</li>
      <li>Click Preview to review the changes before they go live.</li>
      <li>If everything looks right, click Confirm to save the changes.</li>
    </ol>
    <h3>Column reference for this update</h3>
    <table class="ref-table">
      <thead><tr><th>Column</th><th>Notes</th></tr></thead>
      <tbody>
        <tr><td>ID</td><td>Required identifier — do not edit</td></tr>
        <tr><td>Name</td><td>Only if changing the unit number</td></tr>
        <tr><td>Vehicle Regulation Mode</td><td>Enter Regulated or Unregulated</td></tr>
        <tr><td>Asset Attribute: CMV</td><td>Set to CMV for every row marked Regulated</td></tr>
      </tbody>
    </table>
    <div class="callout tip"><strong>Practical recommendation</strong><p>If your updates include unit number/name changes, regulated/unregulated changes, and attribute changes together, use the Gateway CSV bulk edit for the affected vehicles first — that's the one workflow that clearly covers all three at once.</p></div>