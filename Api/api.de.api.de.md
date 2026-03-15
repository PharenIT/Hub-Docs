---
title: List objects
description: Lists all system-defined and user-defined objects in your workspace.
---

# List objects

Lists all system-defined and user-defined objects in your workspace.

Required scopes: `object_configuration:read`.

::docs-api-endpoint
---
method: "GET"
path: "/v2/objects"
title: "List objects"
description: "Returns all objects in your workspace."
---
::

## Request (cURL)

```bash
curl --request GET \
  --url https://api.example.com/v2/objects \
  --header 'Authorization: Bearer <token>'