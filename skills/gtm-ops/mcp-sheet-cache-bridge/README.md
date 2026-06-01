# MCP Sheet Cache Bridge

Keep Zapier Tables as the source of truth while Google Sheets-based tools read a lightweight cache tab.

## Use When

Use this when a team has moved operational data out of a spreadsheet and into Zapier Tables, but still needs Google Sheets-based scripts, dashboards, exports, or digests to keep working.

## What It Does

- Mirrors only the fields a downstream Sheet-based tool needs.
- Syncs cache rows when source records change.
- Lets Apps Script, Looker Studio, formulas, or simple exports read from the Google Sheet cache.
- Avoids scheduled full-table refreshes that burn tasks.
- Keeps the authoritative record in Zapier Tables.

## Inputs

- Zapier Table or MCP-connected record store.
- Cache tab schema.
- Record ID or external join key.
- Filter rules for which records should appear in the cache.
- Google Sheet cache destination.

## Outputs

- Google Sheet cache tab with current rows.
- Documented field map.
- Event-driven sync rules.
- Optional digest, dashboard, or export read path.

## Setup

1. Read `SETUP.md` for Zapier MCP and Google Sheets setup.
2. Copy `SKILL.md` into your agent skill directory.
3. Adapt `SCHEMA-MAP.md` to your source table and cache tab.
4. Run `ONBOARDING-PROMPT.md` before the first production sync.

## Safety

Do not delete cache tabs, disable legacy read paths, or change schema mappings without explicit human approval. Keep private customer, employee, and operational data out of examples.

## Inspired By

Generalized from a public workflow by Kenny Taber, who moved a multi-tab operational pipeline into Zapier Tables while keeping lightweight Google Sheets reads available for existing scripts and digests.
