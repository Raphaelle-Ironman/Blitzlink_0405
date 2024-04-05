[service-blitzlink](../../../README.md) / [API](../README.md) / [Projects](./README.md) / Get an url

# Get an url

Get an url by id.

```
GET /projects/:id_project/urls/:id_url
```

## Parameters

| Name         | Description        |
|--------------|--------------------|
| `id_project` | ID of the project. |
| `id_url`     | ID of the url.     |

## Example

```
GET /projects/3/urls/1
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
  "id": 1,
  "project_id": 3,
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
}

```
