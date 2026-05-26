# Customer Deck Builder Setup

## Required Connections

- Zapier MCP
- Gamma actions in Zapier MCP:
  - Create Generation
  - Get Generation Status
- Approved CRM or account-data source
- Approved usage or product-adoption source
- Optional meeting notes, research docs, or customer-success tracker

## Zapier MCP Setup

1. Open your Zapier MCP configuration.
2. Add or enable Gamma.
3. Enable the Create Generation action.
4. Enable the Get Generation Status action.
5. Add the approved CRM, account-data, document, and meeting-context actions your team is allowed to use.
6. Confirm the agent can read only the fields needed for deck creation.

## Data Mapping

Map your local systems to the fields in `SCHEMA-MAP.md`. Keep the mapping at the category level in this public skill package. Store private SQL, table names, and access details in your own private implementation repo.

## First Safe Test

1. Pick a test account or sanitized sample.
2. Ask the agent to generate only a deck outline.
3. Review the outline for private data, unsupported claims, and customer-facing tone.
4. Generate a Gamma deck only after the outline is approved.
5. Review the Gamma deck before sharing externally.

## Approval Gates

- Approve the data snapshot before writing slides.
- Approve the slide outline before generating in Gamma.
- Approve the generated deck before customer sharing.
- Require extra review for renewal terms, roadmap claims, customer proof, logos, quotes, or metrics.
