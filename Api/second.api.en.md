---
description: Creates a new post using a public API.
title: Create post
---

# Create post

## ::docs-api-endpoint

method: "POST" path: "https://jsonplaceholder.typicode.com/posts" title:
"Create post" description: "Creates a new post using the JSONPlaceholder
public API." --- ::

## Input fields

  Name     In     Type     Required   Description
  -------- ------ -------- ---------- ---------------------
  title    body   string   yes        Title of the post
  body     body   string   yes        Content of the post
  userId   body   int      yes        ID of the author

## Request body schema

``` json
{
  "title": "My first API post",
  "body": "This is an example post created via the API.",
  "userId": 1
}
```

## Example request

``` bash
curl -X POST https://jsonplaceholder.typicode.com/posts \
  -H "Content-Type: application/json" \
  -d '{
    "title": "My first API post",
    "body": "This is an example post created via the API.",
    "userId": 1
  }'
```
