# MCP Sheet Cache Bridge Schema Map

Use this map to adapt the skill to your source table and cache tab.

## Source Record Store

- source system
- source object or table
- record ID
- active-record filter
- deleted-record handling
- update timestamp

## Cache Tab

- spreadsheet name
- tab name
- record ID column
- display columns
- owner or assignee column
- status column
- source link column
- last synced column

## Field Mapping

| Source field | Cache column | Required | Notes |
| --- | --- | --- | --- |
| record ID | record_id | Yes | Stable join key |
| title or label | display_title | Yes | Human-readable row |
| status | status | Optional | Used for filters and digests |
| priority | priority | Optional | Used for sort order |
| owner | assignee | Optional | Team or person |
| source URL | link | Optional | Link back to source |
| updated timestamp | updated_at | Yes | Last sync timestamp |

## Do Not Mirror

- credentials
- private notes
- sensitive customer or employee data
- raw email bodies
- payment or billing details
- fields not needed by downstream consumers
