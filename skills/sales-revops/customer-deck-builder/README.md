# Customer Deck Builder

## Use When

Use this when a sales, customer success, or onboarding team needs a customer-facing deck for a discovery call, QBR, renewal, expansion conversation, executive briefing, onboarding kickoff, or follow-up.

## What It Does

Turns approved account context, usage signals, meeting goals, and use-case guidance into a structured customer deck, then uses Zapier MCP to generate the presentation in Gamma.

## Inputs

- Company name, domain, or account ID
- Call type and meeting goal
- Attendee roles or titles
- Approved account, product usage, CRM, and renewal context
- Optional meeting notes, research docs, or specific topics

## Outputs

- Deck outline and narrative
- Slide-by-slide markdown for Gamma
- Gamma presentation URL
- Short summary of the deck
- Review notes for slides that need manual refinement

## Setup

1. Read `SETUP.md` for Zapier MCP and Gamma configuration.
2. Copy `SKILL.md` into your agent skill directory.
3. Adapt `metadata.yaml` and `SCHEMA-MAP.md` to your approved data sources.
4. Run `ONBOARDING-PROMPT.md` before the first real customer deck.

## Safety

Keep a human review step before sharing with customers. Do not expose raw account exports, internal IDs, private usage details, personal emails, private notes, or unsupported product claims in a customer-facing deck.
