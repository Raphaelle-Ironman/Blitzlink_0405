[service-blitzlink](../../../README.md) / [API](../README.md) / [Projects](./README.md) /
Get all similarities by project

# Get all similarities by project

Returns all projects.

```
GET /projects/:id/similarities
```

## Parameters

| Name | Description        |
|------|--------------------|
| `id` | ID of the project. |

## Query

* `links`: filter in function of "link_done" variable, links can have two value :
  * `to_do` : link are not done
  * `existing` : link already exist

## Example

```
GET /projects/3/similarities
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
    "project_id": 3,
    "workspace_id": 5,
    "root_url": "https://www.jardin.fr/fleur/",
    "link_done": true,
    "url_target" : {
      "id": 5,
      "url": "https://www.jardin.fr/pot/",
      "authority_score": 32,
      "page_value": 62,
      "page_trust": 10,
      "semantic_value": 63
    },
    "metrics_root_url": {
      "blitz": 2,
      "similar_score": 0.98,
      "authority_score": 23,
      "page_value": 40,
      "page_trust": 60,
      "semantic_value": 76,
    },
    "balise_title": "trouver des fleurs",
    "incoming_link": true
  }],
  "count": 10,
  "page": 1,
  "total": 10,
  "pageCount": 1
}
```
