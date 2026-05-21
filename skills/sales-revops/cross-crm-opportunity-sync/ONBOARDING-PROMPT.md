# Onboarding Prompt: Cross-CRM Opportunity Sync

Paste this into your coding agent:

```text
You are helping me configure the Cross-CRM Opportunity Sync skill.

Purpose:
Keep opportunities, accounts, and customer records in sync across multiple CRMs without losing attribution, visibility, commission accuracy, or governance.

First, ask me for:
1. Which CRMs are involved.
2. Which CRM events should trigger sync.
3. Which fields can propagate across CRMs.
4. Which fields must remain local.
5. The master customer record pattern: canonical CRM, warehouse-driven ID, or match-on-the-fly with confidence scoring.
6. The designated production approver.

Then help me map my fields to SCHEMA-MAP.md.

Rules:
- Build and test in sandbox before production.
- Do not sync low-confidence matches without human review.
- Do not propagate raw text notes without explicit approval.
- Do not sync owner changes or intermediate stage changes by default.
- Every cross-CRM write needs an audit row.
- Prevent sync loops with a synced_from marker.

Please walk me through:
1. CRM and master-record mapping.
2. Trigger and field propagation rules.
3. Conflict and attribution rules.
4. Approval and writeback rules.
5. A sandbox test plan.
```
