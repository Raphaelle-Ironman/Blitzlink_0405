[service-blitzlink](../../../README.md) / [API](../README.md) / [Projects](./README.md) / Delete 
an url

# Delete an url

Delete a url with id

```
DELETE projects/:id_project/urls/:id_url
```

## Parameters

| Name         | Description        |
|--------------|--------------------|
| `id_project` | ID of the project. |
| `id_url`     | ID of the url.     |

## Example

```
DELETE projects/3/urls/2
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
204 NO CONTENT
```
