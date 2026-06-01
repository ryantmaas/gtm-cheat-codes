# MCP Media Inbox Triage Setup

## Required Connections

- Zapier MCP.
- Gmail shared inbox or label.
- Slack channel for triage summaries or urgent alerts.
- Google Sheet for the persistent triage log.
- LLM with structured output support.

## Step 1: Configure Gmail

Enable Gmail actions through Zapier MCP:

| Action | Purpose |
| --- | --- |
| Search email | Find new or unresolved messages |
| Read email/thread | Pull minimal context for classification |
| Create draft | Draft suggested replies for human approval |
| Add label | Mark reviewed messages when approved |

Start with a bounded query:

```text
to:{SHARED_INBOX} newer_than:1d -label:triaged
```

## Step 2: Configure Slack

Create a dedicated triage channel and set posting rules:

| Message type | Destination |
| --- | --- |
| High urgency | Immediate Slack alert |
| Medium urgency | Daily triage summary |
| Low urgency | Daily or weekly digest |
| Ignore/spam | Google Sheets log only |

Do not post full email bodies to Slack.

## Step 3: Create The Google Sheets Log

Create columns:

| Column | Purpose |
| --- | --- |
| received_at | Message timestamp |
| sender_name | Human-readable sender |
| sender_email_domain | Domain only if privacy matters |
| subject | Email subject |
| category | Classification |
| urgency | High / Medium / Low / Ignore |
| summary | One-sentence ask |
| suggested_owner | Team or person |
| suggested_next_action | Concrete next step |
| gmail_thread_link | Source link |
| status | New / Routed / Done / Ignored |

## Step 4: Configure Routing

Start with:

```yaml
media_request: PR
partnership_inquiry: Partnerships
customer_community_lead: Community
urgent_executive_risk: Leadership
vendor_pitch: Ignore or weekly digest
spam_no_action: Ignore
unclear: Human review
```

Customize owners for your team.

## Step 5: Test

Run the agent against a small sample:

- real media request
- partnership inquiry
- customer or community note
- generic vendor pitch
- spam message
- vague message that should route to human review

Tune false positives, false negatives, blocklists, whitelists, urgency rules, and owner routing after the first week.

## Approval Gates

- Human review before sending any reply.
- Human review before archiving or labeling messages automatically.
- Human review before posting sensitive summaries to broad channels.
- Human approval before adding new owner-routing rules.
