# Componesnt Examples (MDC Syntax)


![J Kanthak-04.png](/_assets/1773572035902-J-Kanthak-04.png)


Here is a ready-to-use cheat sheet for the new documentation components. You can copy and paste these blocks directly into your Markdown (`.md`) files in the `PharenIT/Hub-Docs` repository.
# Willkommen in den Docs!

Schau dir dieses Feature an:

::docs-feature-card
---
title: "Tolles Feature"
icon: "lucide:rocket"
---
Dieser Text steht innerhalb der Karte als Body und wird komplett vom MDC durchgereicht!
::
## Feature Cards

Use feature cards to link to other pages with a nice hover effect.

```md
::docs-feature-card
---
title: Workflows
description: Automate your processes with our visual workflow builder and simple node-based architecture.
icon: lucide:git-merge
badge: Core Feature
href: /docs/workflows
---
::
```

## Callouts

Use callouts to highlight important information. Available types: `note`, `info`, `success`, `warning`, `danger`.

```md
::docs-callout
---
type: info
title: Did you know?
---
You can use standard Markdown inside callouts, like **bold**, *italic*, or `code`.
::

::docs-callout
---
type: warning
title: Proceed with caution
---
Deleting a workflow cannot be undone. Make sure to export your config first.
::
```

## Steps

Perfect for tutorials or setup guides.

```md
::docs-steps
:::docs-step
---
number: 1
title: Create a new workspace
---
Head over to your dashboard and click the **New Workspace** button.
:::

:::docs-step
---
number: 2
title: Invite your team
---
Navigate to the team settings and invite members via email.
:::

:::docs-step
---
number: 3
title: Build your first workflow
---
Go to the Flow editor and drag your first node onto the canvas.
:::
::
```

## Accordion / FAQ

Great for grouping FAQs or hiding large amounts of optional details.

```md
::docs-accordion
:::docs-accordion-item
---
value: item-1
title: Wie viel kostet die Plattform?
---
Wir bieten eine kostenlose Version für bis zu 5 Mitglieder an. Danach 10€ pro Nutzer/Monat.
:::

:::docs-accordion-item
---
value: item-2
title: Bieten Sie Enterprise-Support an?
---
Ja! Kontaktieren Sie unser Vertriebsteam für maßgeschneiderte SLAs.
:::
::
```

## API Endpoint with Playground Dialog

Shows a clean endpoint row that opens a detailed "Try it" dialog containing your examples and any extra markdown content.

```md
::docs-api-endpoint
---
method: POST
path: /api/v1/workflows/execute
title: Execute a workflow
description: Trigger a workflow execution manually with custom input data.
requestExample: "curl -X POST https://api... -d '{\"inputs\": {}}'"
responseExample: "{\n  \"status\": \"running\"\n}"
---

#content
Here you can document additional parameters that will appear inside the interactive Dialogue.

| Parameter | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `workflow_id` | `string` | Yes | The UUID of the workflow to run. |
| `inputs` | `object` | No | Optional key-value pairs to pass to the workflow. |

::
```
