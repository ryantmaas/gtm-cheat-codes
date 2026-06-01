# MCP Sheet Cache Bridge Setup

## Required Connections

- Zapier MCP.
- Zapier Tables or another approved MCP-connected record store.
- Google Sheets.
- Optional Slack for digest or sync-health updates.

## Step 1: Choose The Source Of Truth

Pick the table or record store that should own the canonical data. Document:

- source object or table name
- stable record ID
- fields needed by the cache
- fields that should never be mirrored
- active-record filter

## Step 2: Create The Google Sheet Cache

Create one cache tab for the downstream read path. Start with:

| Column | Purpose |
| --- | --- |
| record_id | Source row ID or external join key |
| display_title | Subject, name, or primary label |
| status | Filter or workflow state |
| priority | Sort order |
| assignee | Owner or team |
| link | Source link |
| updated_at | Last sync timestamp |

## Step 3: Configure Zapier MCP Actions

Enable the approved actions needed to:

- read source records
- find a row in Google Sheets by record ID
- create a row in Google Sheets
- update a row in Google Sheets
- delete or clear a row in Google Sheets

Use least-privilege connections and keep the cache in a controlled folder.

## Step 4: Define Sync Logic

Use this decision path:

1. If a changed source record matches the active cache filter, upsert the matching cache row.
2. If it no longer matches the filter, remove or clear the matching cache row.
3. If the source record is deleted, remove the matching cache row.
4. If the cache row cannot be found, create it only when the active filter still matches.

## Step 5: Test Safely

1. Copy a small sample into a test table.
2. Sync into a test cache tab.
3. Verify creates, updates, filter exits, and deletes.
4. Point one downstream script or dashboard at the cache.
5. Run a cutover review before production.

## Approval Gates

- Schema map approval before production sync.
- Delete-path approval before enabling cache row deletes.
- Cutover approval before turning off legacy spreadsheet entry.
- Human approval before posting customer-facing or broad team digests.
