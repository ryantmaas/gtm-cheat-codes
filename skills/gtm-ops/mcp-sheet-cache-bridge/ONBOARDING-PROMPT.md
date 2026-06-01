# MCP Sheet Cache Bridge Onboarding Prompt

Use this prompt before the first implementation.

```text
You are setting up an MCP Sheet Cache Bridge.

Goal:
Keep Zapier Tables or another approved MCP-connected record store as the source of truth while Google Sheets-based scripts, dashboards, exports, or digests read a lightweight cache tab.

Before building anything, confirm:

1. What is the source record store?
2. What is the stable record ID?
3. Which records should appear in the cache?
4. Which fields does the downstream Sheet-based tool actually need?
5. Which fields must never be mirrored?
6. Should records that leave the filter be deleted or cleared from the cache?
7. Who approves schema changes and delete-path behavior?

Produce:

- source-to-cache field map
- cache tab schema
- sync decision table
- first safe test plan
- approval gates

Do not delete rows, disable legacy read paths, or change production schema without explicit human approval.
```
