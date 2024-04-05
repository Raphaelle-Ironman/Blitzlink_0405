[service-blitzlink](../../../README.md) / [API](../README.md) / [Projects](./README.md) / 
Export similarities by url

# Export similarities by project

Returns all similarities.

```
GET /projects/:idProject/export-similarities
```

## Parameters

| Name         | Description        |
|--------------|--------------------|
| `id_project` | ID of the project. |
| `id_url`     | ID of the url.     |

## Queries

`ids[]` : id of the backlinks to export. Must be repeat to have multiple backlinks

## Example

```
GET /projects/3/export-similarities
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

```csv
id,project_id,workspace_id,root_url,link_done,url_target,similar_score,root_url_bas,root_url_page_value,root_url_page_trust,root_url_semantic_value,balise_title,incoming_link
1076,2,5,https://www.jardin.fr/,false,https://www.jardin.fr/test,97,36,59,19,48,mon beau jardin,false
```