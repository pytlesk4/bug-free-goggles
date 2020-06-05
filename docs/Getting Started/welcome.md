---
tags: [something]
---

# Creating an API Token

To get started, you'll need to create an API token to access our API:

```json json_schema
{
 "title": "User",
 "type": "object",
 "properties": {
   "id": {
     "type": "string"
   },
   "name": {
     "type": "string",
     "description": "The user's full name."
   },
   "age": {
     "type": "number",
     "minimum": 0,
     "maximum": 150
   }
 },
 "required": [
   "id",
   "name"
 ]
}
```

<!-- theme: danger -->

> ### Mission Accomplished!
>
> Here is my success callout!

```json http
{
  "url": "/accessToken",
  "baseUrl": "http://localhost:8080",
  "method": "post",
  "headers": {
    "testHeader": "testHeaderValue"
  },
  "query": {},
  "body": {
    "username": "myuser",
    "password": "mypassword"
  }
}
```

Once you have the token, you can then issue requests to the API:

```json http
{
  "baseUrl": "http://localhost:8080",
  "method": "get",
  "url": "/requestResource",
  "headers": {
    "Authorization": "my token"
  },
  "query": {
    "testQueryParam": [
      "testQueryValue"
    ]
  },
  "body": {
    "name": "body",
    "value": 5,
    "isValid": true
  }
}
```
