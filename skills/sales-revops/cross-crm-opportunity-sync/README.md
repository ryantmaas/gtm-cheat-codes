# Cross-CRM Opportunity Sync

Customer story: [Voltt / William Ascough](https://zapier.com/blog/voltt-operators-integration), consulting Cyncly and other acquisition-built GTM organizations.

## Use When

Use this when a business runs multiple CRMs and a single customer, account, or deal can touch more than one system.

## What It Does

Keeps opportunities, accounts, and customer records in sync across CRMs while preserving attribution, ownership, commission visibility, and governance.

## Inputs

- CRM opportunity or stage-change event
- Account and customer record details
- Master customer record or matching rules
- Sync rules and canonical stage mapping
- Attribution and commission rules

## Outputs

- Mirrored opportunity or linked record
- Cross-CRM context for the rep
- Bundle or shared-deal coordination fields
- Audit trail entry
- Human-review queue for conflicts and low-confidence matches

## Setup

1. Read `SETUP.md` for Zapier MCP and governance setup.
2. Copy `SKILL.md` into your agent skill directory.
3. Adapt `metadata.yaml` and `SCHEMA-MAP.md` to your CRM stack.
4. Run `ONBOARDING-PROMPT.md` before the first sandbox workflow.

## Safety

Use a sandbox-to-production gate. Do not sync fuzzy matches, revenue fields, commission-sensitive fields, raw notes, or customer data into production without the required human approval.

## Inspired By

This skill is generalized from [When operators get the keys to the integration stack](https://zapier.com/blog/voltt-operators-integration), a customer story with Voltt founder William Ascough. The reference implementation supports a global multi-product business, including Cyncly, with multiple CRMs and an operator-led governance model for production workflows.

Voltt: GTM systems architecture for the AI era. [volttconsulting.co.uk](https://volttconsulting.co.uk)
