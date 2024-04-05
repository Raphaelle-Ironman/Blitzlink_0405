[service-notorious](../../../README.md) / [API](../README.md) / [How to use](./README.md) / Pagination

# Pagination

Results of requests with list have a pagination system. The page number can be selected with the
key `page` in json query field `q`. The reponse's body `pagination` property give information about the total number
of pages, the number of elements by pages and the current page.
The number of entries by page can be selected by the key `amount` in json query field `q`.

## Example

```
GET /projects?q={"page":2,"amount":3}
```

Response

```
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
  },...],
  "count": 3,
  "page": 2,
  "total": 16,
  "pageCount": 6
}
```
