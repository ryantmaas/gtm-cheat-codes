# MCP Media Inbox Triage

Find media, partnership, and high-intent requests buried in a shared inbox, summarize the useful ones, and route them to the right owner.

## Use When

Use this when a shared inbox receives a mix of press requests, creator pitches, partnership offers, customer notes, newsletters, and vendor spam, and a human currently has to read everything to find the few messages worth acting on.

## What It Does

- Searches Gmail for new or unresolved messages in a bounded window.
- Classifies each message by request type and urgency.
- Extracts the actual ask, deadline, organization, suggested owner, and next action.
- Routes useful messages to Slack, Google Sheets, or a triage doc.
- Drafts replies for human review when a response is needed.

## Inputs

- Gmail shared inbox or label.
- Search window.
- Routing rules.
- Owner map.
- Slack channel and Google Sheets log destination.

## Outputs

- Slack triage summary.
- Persistent Google Sheets triage log.
- Suggested owner and next action.
- Optional Gmail draft for human review.
- Weekly volume and time-saved report.

## Setup

1. Read `SETUP.md` for Zapier MCP setup.
2. Copy `SKILL.md` into your agent skill directory.
3. Adapt `SCHEMA-MAP.md` to your inbox, routing, and log.
4. Run `ONBOARDING-PROMPT.md` before the first live triage run.

## Safety

Never auto-send replies. Do not expose full private email bodies in Slack or public docs. Use Gmail links as the source of truth and route unclear messages to human review.

## Inspired By

Generalized from Matt Canning, Founder and CEO of [NoPlex](https://noplex.ai/), whose team uses Zapier MCP and Gmail to scan a media inbox for relevant requests. The workflow reduced human inbox review from about 4 hours per week to about 15 minutes.
