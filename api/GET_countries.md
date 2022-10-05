## GET `api/countries`

---

### Description

This method is used to retreive list of supported countries.

---

### Request

No payload required.

---

### Response

```
[
  {
    "code": "ae",
    "nodes_count": 1
  },
  
  <...>,
  
  {
    "code": "us",
    "nodes_count": 928
  }
]
```

| Parameter   | Type        | Description                                    |
|-------------|-------------|------------------------------------------------|
| code        | String      | Country code in accordance with ISO 3166-2     |
| nodes_count | Int         | Number of nodes available in this country      |

---

### Errors

| Error Message                   |
|---------------------------------|
| UnknownError                    |
