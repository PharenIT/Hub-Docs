---
title: Create object
description: Erstellt ein neues Objekt.
---

# Create object

::docs-api-endpoint
---
method: "POST"
path: "/v2/objects"
title: "Create object"
description: "Creates a new object."
---
::

## Input fields

| Name         | In    | Type   | Required | Description                |
|--------------|-------|--------|----------|----------------------------|
| name         | body  | string | yes      | Objektname                 |
| api_slug     | body  | string | yes      | Eindeutiger API-Slug       |
| description  | body  | string | no       | Beschreibung               |
| dry_run      | query | bool   | no       | Validierung ohne Schreiben |

## Request body schema

```json
{
  "name": "People",
  "api_slug": "people",
  "description": "CRM Kontakte"
}
