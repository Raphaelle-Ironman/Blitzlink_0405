[service-blitzlink](../../../README.md) / [API](../README.md) / [Projects](./README.md) / 
Delete a project

# Delete a project

Delete a project with id

```
DELETE /projects/:id
```

## Parameters

| Name | Description        |
|------|--------------------|
| `id` | ID of the project. |

## Example

```
DELETE /projects/1
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
