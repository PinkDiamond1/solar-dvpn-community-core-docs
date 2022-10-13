## GET `api/continents`

---

### Description

This method is used to retreive list of supported continents with their number of nodes.

---

### Request

No payload required.

---

### Response

```
[
  {
    "code": "AF",
    "nodes_count": 0
  },
  
  <...>,
  
  {
    "code": "EU",
    "nodes_count": 948
  }
]
```

| Parameter   | Type        | Description                                    |
|-------------|-------------|------------------------------------------------|
| code        | String      | Two-letter continent code                      |
| nodes_count | Int         | Number of nodes available in this continent    |

---

### Errors

| Error Code | Reason Phrase           | Description                             |
|------------|-------------------------| ----------------------------------------|
| 500        | Some backend message    |                                         |

