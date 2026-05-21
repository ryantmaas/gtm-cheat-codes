# Schema Map

Map these fields to your own helpdesk, issue tracker, knowledge base, CRM, or Zapier Tables setup.

| Field | Required | Notes |
| --- | --- | --- |
| ticket_id | Yes | Helpdesk ticket ID or URL. |
| ticket_subject | Yes | Customer-visible ticket subject. |
| ticket_body | Yes | Initial customer issue description. |
| comment_thread | Yes | Conversation history and attempted fixes. |
| requester | Yes | Requester and organization context. |
| product_area | No | Product or feature area used to narrow searches. |
| priority | No | Helpdesk priority, severity, plan tier, or SLA indicator. |
| similar_tickets | No | Related tickets and resolutions. |
| matched_defects | No | Matching issue tracker records. |
| matched_feature_requests | No | Matching feature backlog records. |
| knowledge_base_matches | No | Relevant docs, runbooks, and troubleshooting guides. |
| classification | Yes | Known defect, feature gap, configuration issue, performance issue, or novel issue. |
| recommended_next_action | Yes | Rep-facing action recommendation. |
| customer_reply_draft | No | Draft reply requiring rep review before sending. |
| escalation_packet | No | Engineering or product escalation packet requiring approval. |
