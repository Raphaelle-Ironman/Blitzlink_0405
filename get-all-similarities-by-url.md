[service-blitzlink](../../../README.md) / [API](../README.md) / [Projects](./README.md) /
Get all similarities by url

# Get all similarities by url

Returns all similarities by url.

```
GET /projects/:idProject/urls/:idUrl/similarities
```

## Parameters

| Name         | Description        |
|--------------|--------------------|
| `id_project` | ID of the project. |
| `id_url`     | ID of the url.     |

## Query

* `links`: filter in function of "link_done" variable, links can have two value :
  * `to_do` : link are not done
  * `existing` : link already exist

## Example

```
GET /projects/3/urls/2/similarities
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
      "id": 2,
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
