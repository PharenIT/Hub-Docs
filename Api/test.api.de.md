---
description: Returns a random cat fact.
title: Get cat fact
---

# Get cat fact

## ::docs-api-endpoint

method: "GET" path: "https://catfact.ninja/fact" title: "Get cat fact"
description: "Returns a random cat fact from the Cat Facts public API."
--- ::

## Input fields

  -------------------------------------------------------------------------------
  Name         In      Type      Required   Description
  ------------ ------- --------- ---------- -------------------------------------
  max_length   query   integer   no         Maximum length of the returned cat
                                            fact

  -------------------------------------------------------------------------------

## Example request

``` bash
curl https://catfact.ninja/fact
```

## Example request with parameters

``` bash
curl "https://catfact.ninja/fact?max_length=100"
```

## Example response

``` json
{
  "fact": "Cats have five toes on their front paws, but only four on the back ones.",
  "length": 67
}
```

## Response fields

  Name     Type     Description
  -------- -------- -----------------------------
  fact     string   The random cat fact
  length   number   Length of the returned fact
