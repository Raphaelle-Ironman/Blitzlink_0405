[service-blitzlink](../../../README.md) / [API](../README.md) / [Projects](./README.md) / Create an url

# Create an url

Add new url to analyzed in the project

```
POST /projects/:id_project/urls
```

## Body

* `user`: Details of the user the request is being done for. See [User management](../how-to-use/user-management.md),
* `data`:
  * `url`: url to analyzed

## Example

```
POST /projects/3/urls
```

```json
{
  "user": {
    "workspaces": [5],
    "role": "customer"
  },
  "data": {
    "url": "https://jardin.fr/jardin-interieur",
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
  "project_id": 3, 
  "workspace_id": 5,
  "url": "A title",
  "created_at": "2022-11-30 10:10:10",
}
```
