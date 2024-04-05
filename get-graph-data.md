[service-blitzlink](../../../README.md) / [API](../README.md) / [Projects](./README.md) / Get graph data

# Get graph data

Give data to create the network graph.

```
GET /projects/:id/graph
```

## Parameters

| Name | Description        |
|------|--------------------|
| `id` | ID of the project. |

## Query

* `blitzlimit`: add a limit for the number of link to sent.
* `links`: filter in function of "link_done" variable, links can have two value :
  * `to_do` : link are not done
  * `existing` : link already exist

## Example

```
GET /projects/3/graph
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
  "graph_data": {
    "urls": [
      {
        "id": 1,
        "url": "https://www.eskimoz.co.uk/digital-marketing-agency-startups/",
        "authority_score": 60,
        "page_trust": 50,
        "page_value": 72,
        "semantic_value": 58,
        "category": 1
      },
      {
        "id": 2,
        "url": "https://www.eskimoz.co.uk/digital-marketing-agency-real-estate/",
        "authority_score": 51,
        "page_trust": 37,
        "page_value": 69,
        "semantic_value": 48,
        "category": 1
      }
    ],
    "links" : [
      {
        "source": 1,
        "target": 2,
        "blitz": 4,
        "link_done": true
      }
    ]
  }
}
```

