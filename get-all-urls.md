[service-blitzlink](../../../README.md) / [API](../README.md) / [Projects](./README.md) / Get urls

# Get all urls

Get urls with metrics in projects.

```
GET /projects/:id/serps-pages
```

## Parameters

| Name | Description        |
|------|--------------------|
| `id` | ID of the project. |

## Example

```
GET /projects/4/urls
```

```json
{
  "user": {
    "id": 1,
    "workspaces": [5],
    "role": "customer"
  }
}
```

Response

```
200 OK
```

```json
{
  "data": [{
      "id": 1,
      "project_id": 4,
      "workspace_id": 5,
      "created_at": "2022-11-30 10:10:10",
      "url": "https://www.jardin.fr/pot/" ,
      "state": "ip",
      "metrics": {
        "bas": 23,
        "page_value": 40,
        "page_trust": 60,
        "semantic_value": 76,
      },
      "link_to_do_by_url": 3,
  }],
  "count": 3,
  "page": 1,
  "total": 3,
  "pageCount": 1
}
```
