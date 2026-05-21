# Setup: Cross-CRM Opportunity Sync

## Required Systems

- Zapier MCP
- Two or more CRMs
- Master customer record source
- LLM connection for matching and enrichment
- Sandbox or staging environment
- Designated production approver

## Optional Systems

- Data warehouse
- Team chat for notifications
- Finance or commission system
- Email enrichment tool

## Zapier MCP Setup

1. Create a Zapier MCP server at `https://mcp.zapier.com`.
2. Add only the CRM actions needed for the workflow.
3. Equip read/create/update actions for accounts, opportunities/deals, companies, and contacts as needed.
4. Equip an LLM action for matching and enrichment.
5. Equip a master record lookup source such as a canonical CRM, warehouse, or approved matching workflow.
6. Test in read-only mode, then sandbox writes, before production writes.

## Zapier SDK Setup

Use Zapier SDK when the sync becomes a production workflow with state, retries, logs, schedules, audit rows, sandbox-to-production promotion, or repeatable reconciliation logic.

## First Safe Test

Build the first version in sandbox and test against 10 deals:

- Standard new opportunity
- Bundled deal across CRMs
- Deal that changes owner
- Deal that gets split
- Deal that gets merged
- Low-confidence customer match
- Currency or stage taxonomy mismatch

Promote only after the designated approver signs off.

## Review Gates

- Sandbox-to-production approval before production writes.
- Human review for fuzzy customer matches.
- Finance review for revenue or commission-sensitive workflows.
- Compliance review for customer-data workflows above the approved threshold.
