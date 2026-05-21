# Schema Map

Map these fields to your own CRMs, warehouse, master customer record, or Zapier Tables setup.

| Field | Required | Notes |
| --- | --- | --- |
| source_crm | Yes | CRM where the triggering event occurred. |
| target_crm | Yes | CRM that may need a mirrored or linked record. |
| source_opportunity_id | Yes | Deal or opportunity ID in the source CRM. |
| target_opportunity_id | No | Existing or newly created matching opportunity in the target CRM. |
| source_account_id | Yes | Source CRM account or company ID. |
| master_customer_id | Yes | Canonical customer ID or reviewed match ID. |
| match_confidence | Yes | Confidence score for customer matching. |
| sync_trigger | Yes | Approved trigger such as opportunity_created or stage_change_to_closed_won. |
| bundle_id | No | Shared ID for bundled or cross-business-unit deals. |
| canonical_stage | No | Mapped stage in the canonical taxonomy. |
| amount | No | Amount and currency handling must follow approved rules. |
| close_date | No | Close date to propagate when approved. |
| attribution_source | Yes | Originating CRM, closing CRM, or approved attribution owner. |
| synced_from | Yes | Marker used to prevent sync loops. |
| audit_row_id | Yes | Audit trail row for the write. |
| review_status | Yes | Draft, sandbox, needs review, approved, promoted, or blocked. |
