---
title: API Explorer Showcase
description: Ein Showcase für den interaktiven API Playground in Pharen Docs.
order: 10
---

# API Explorer Showcase

Diese Seite demonstriert die Nutzung des `::docs-api-endpoint` Komponenten. Du kannst APIs direkt in der Dokumentation testen.

## Einfacher API-Aufruf

Hier ist ein Beispiel für eine öffentliche API (The Free Joke API), die wir direkt hier ausprobieren können.

::docs-api-endpoint
---
title: Get a Random Joke
method: GET
baseUrl: https://official-joke-api.appspot.com
path: /random_joke
description: Ruft einen zufälligen Witz von der Official Joke API ab.
---
::

## API mit Parametern

Du kannst auch Endpunkte mit Query-Parametern definieren.

::docs-api-endpoint
---
title: Search Github Repos
method: GET
baseUrl: https://api.github.com
path: /search/repositories
params:
  - name: q
    type: string
    description: Search query (e.g. "topic:nuxt")
    required: true
    default: topic:nuxt
  - name: sort
    type: string
    description: Sort by stars, forks, etc.
    default: stars
description: Sucht nach Repositories auf GitHub.
---
::

## API Dokumentation mit Antworten

Du kannst auch erwartete Antworten dokumentieren.

::docs-api-response
---
status: 200
description: Erfolgreiche Antwort
---
```json
{
  "id": 1,
  "type": "general",
  "setup": "What do you call a fake noodle?",
  "punchline": "An impasta."
}
```
::

::docs-api-response
---
status: 404
description: Nicht gefunden
---
```json
{
  "error": "Not Found"
}
```
::
