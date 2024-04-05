[service-blitzlink](../../../README.md) / [API](../README.md) / [Projects](./README.md) /
Get all projects

# Get all projects

Returns all projects.

```
GET /projects
```

## Example

```
GET /projects?workspace-id=5
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
    "created_by_id": 2,
    "workspace_id": 5,
    "name": "A title",
    "created_at": "2022-11-30 10:10:10",
    "error": "all",
    "urls": [{
      "id": "5",
      "url": "https://www.jardin.fr/pot/",
      "created_at": "2022-11-30 10:10:10",
      "state": "fi",
      "link_to_do_by_url": 3
    }],
    "link_to_do_by_project": 10
  }],
  "count": 10,
  "page": 1,
  "total": 15,
  "pageCount": 2
}
```
