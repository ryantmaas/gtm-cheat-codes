# Support Ticket Triage Agent

Customer story: [ClickUp](https://zapier.com/customer-stories/clickup), inspired by Corey Smith's support triage workflow.

## Use When

Use this when support reps need to research a ticket across a helpdesk, bug tracker, feature backlog, and knowledge base before they can write a useful reply.

## What It Does

Pulls live ticket context through Zapier MCP, searches connected systems in parallel, classifies the issue, and gives the rep a recommended next action.

## Inputs

- Ticket URL, ticket ID, or pasted customer message
- Helpdesk ticket context
- Issue tracker and feature backlog search results
- Knowledge-base or runbook search results
- Optional customer or account context

## Outputs

- Ticket classification
- Matched defects, feature gaps, docs, or similar tickets
- Rep-ready triage summary
- Optional customer reply draft
- Optional escalation packet

## Setup

1. Read `SETUP.md` for Zapier MCP configuration.
2. Copy `SKILL.md` into your agent skill directory.
3. Adapt `metadata.yaml` and `SCHEMA-MAP.md` to your support stack.
4. Run `ONBOARDING-PROMPT.md` before the first real workflow.

## Safety

Keep the rep in control. Do not auto-reply to customers, expose internal references in customer-facing drafts, or create ticket/status changes without approval.

## Inspired By

This skill is generalized from a real implementation by [Corey Smith at ClickUp](https://zapier.com/customer-stories/clickup). Corey built an MCP-powered support triage agent that pulls Zendesk context, searches internal defect tracking and feature backlog data in parallel, classifies the ticket, and serves the rep structured context before they type a reply. The public story reports a reduction from 15 minutes to 4 minutes per ticket across 5,000+ monthly tickets, saving 917+ hours monthly.
