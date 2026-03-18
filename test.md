---
title: Page Showcase
description: Ein Überblick über die Standard-Dokumentations-Features von Pharen.
order: 5
---

# Feature Showcase

Dies ist eine normale Dokumentationsseite, die zeigt, wie du deine Inhalte mit MDC (Markdown Components) in Pharen Docs strukturieren kannst.

## Layout & Formatierung

Der Text wird standardmäßig in einem schönen, lesbaren Prose-Layout dargestellt. Du kannst Standard-Markdown verwenden wie **fett**, _kursiv_ oder [Links](https://pharen.de).

### Komponenten-Showcase

Wir haben einige spezialisierte Komponenten für die Dokumentation entwickelt.

::docs-callout
---
type: info
icon: lucide:info
---
**Pro-Tipp**: Nutze Callouts, um wichtige Informationen hervorzuheben. Sie können `info`, `warning` oder `danger` Typen haben.
::

::docs-callout
---
type: warning
icon: lucide:alert-triangle
---
Achtung: Überspringe niemals das `order` Property im Frontmatter, wenn du eine feste Sortierung in der Sidebar möchtest.
::

### Feature Cards

Ideal für die Übersicht von Funktionalitäten oder Modulen.

::docs-feature-card
---
title: API Explorer
icon: lucide:terminal
description: Interaktive API-Endpunkte direkt in der Dokumentation testen.
link: /docs/api-showcase
---
::

::docs-feature-card
---
title: GitHub Sync
icon: lucide:github
description: Bearbeite Dokumente direkt im Browser und erstelle Pull Requests.
---
::

## Code-Beispiele

Wir unterstützen Syntax-Highlighting für alle gängigen Sprachen.

```typescript
// Ein Beispiel in TypeScript
interface DocPage {
  title: string;
  body: any;
  path: string;
}

const getPage = async (path: string): Promise<DocPage> => {
  return await queryCollection('docs').path(path).first();
};
```

Das war der kleine Rundgang durch die Pharen Docs Features!

![Bild (1).png](/_assets/1773860191268-Bild-1-.png)
