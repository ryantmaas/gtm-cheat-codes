# MCP Media Inbox Triage Schema Map

Use this map to adapt the skill to your inbox, Slack channel, and triage log.

## Gmail Source

- inbox address or label
- search window
- excluded labels
- triaged label
- Gmail thread link

## Email Fields

| Field | Use |
| --- | --- |
| sender_name | Human-readable sender |
| sender_email_domain | Domain-level identity |
| subject | Classification signal |
| received_at | Urgency and SLA |
| body_summary | One-sentence ask |
| thread_count | Follow-up signal |
| gmail_thread_link | Source of truth |

## Classification Fields

| Field | Values |
| --- | --- |
| category | media_request, partnership_inquiry, customer_community_lead, urgent_executive_risk, vendor_pitch, spam_no_action, unclear |
| urgency | high, medium, low, ignore |
| suggested_owner | PR, Community, Marketing, Partnerships, Support, Leadership, Human review, Ignore |
| confidence | high, medium, low |
| draft_reply_needed | true or false |

## Google Sheets Log

- received_at
- sender_name
- sender_email_domain
- subject
- category
- urgency
- summary
- suggested_owner
- suggested_next_action
- gmail_thread_link
- status

## Do Not Store In Public Summaries

- full email body
- private attachments
- personal email addresses unless needed for routing
- legal threats beyond a minimal risk summary
- sensitive customer details
- credentials or private links
