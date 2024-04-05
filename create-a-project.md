[service-blitzlink](../../../README.md) / [API](../README.md) / [Projects](./README.md) / Create a project

# Create a project

Create a project and launch an analyse.

```
POST /projects
```

## Body

* `user`: Details of the user the request is being done for. See [User management](../how-to-use/user-management.md),
* `data`:
  * `workspace_id`: ID of the workspace the project is created for,
  * `name`: Name of the project,
  * `urls`: list of urls

## Example

```
POST /projects
```

```json
{
  "user": {
    "id": 1,
    "workspaces": [5],
    "role": "customer"
  },
  "data": {
    "workspace_id": 5,
    "name": "A title",
    "urls": [
        "https://jardin.fr/jardin-interieur",
        "https://jardin.fr/jardin-exterieur",
    ]
  }
}
```

Response

```
201 Created
```

```json
{
  "id": 1,
  "created_by_id": 1,
  "workspace_id": 5,
  "name": "A title",
  "created_at": "2022-11-30 10:10:10",
  "state": "ip",
  "urls": [{
    "id": 5,
    "url": "https://www.jardin.fr/jardin-interieur/",
    "created_at": "2022-11-30 10:10:10",
    "state": "ip"
  },
  {
    "id": 6,
    "url": "https://www.jardin.fr/jardin-exterieur/",
    "created_at": "2022-11-30 10:10:10",
    "state": "ip"
  }
  ]
}
```

