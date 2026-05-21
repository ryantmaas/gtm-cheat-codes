# Setup: Support Ticket Triage Agent

## Required Systems

- Zapier MCP
- Helpdesk with read access
- Bug or issue tracker with search
- Knowledge base or document source
- Agent harness with MCP support

## Optional Systems

- Feature request tracker
- CRM or customer account source
- Source control for regression investigation
- Observability/APM tool for performance tickets

## Zapier MCP Setup

1. Create a Zapier MCP server at `https://mcp.zapier.com`.
2. Add only the tools needed for your support stack.
3. Connect your helpdesk and enable actions to search tickets, get ticket details, read comments, and get requester or organization info.
4. Connect your issue tracker and enable search/read actions for bugs, feature requests, and linked items.
5. Connect your knowledge base and enable search/read actions for docs and runbooks.
6. Test with read-only work before enabling any ticket updates or writeback.

## Zapier SDK Setup

Use Zapier SDK only when this becomes a repeatable workflow with code, state, schedules, retries, logs, or writeback. Good SDK fits include escalation packet creation, similar-ticket linking, SLA warnings, customer follow-up reminders, and daily triage digests.

## First Safe Test

Run the skill on 10-20 sanitized or approved tickets across categories:

- Known defect
- Feature gap
- Configuration issue
- Performance issue
- Novel issue

Confirm the classification, source links, reply draft quality, and approval gates before using production tickets.

## Review Gates

- Rep approval before customer replies.
- Support lead approval before ticket status or tag changes.
- Engineering or product approval before bug creation or escalation packets.
- Human review before broad team alerts or digest publishing.
