## GET `api/countriesByContinent`

---

### Description

This method is used to retreive list of supported countries of selected continent.

---

### Request

```
GET api/nodes?
    continent=EU
```

| Parameter      | Type        | Description                                                               | Required |
|----------------|-------------|---------------------------------------------------------------------------|----------|
| continent      | String      | Two-letter continent code (`AF`, `SA`, `NA`, `AS`, `EU`, `OC` or `AN`)    | YES      |

---

### Response

```
[
  {
    "code": "at",
    "nodes_count": 1
  },
  
  <...>,
  
  {
    "code": "ua",
    "nodes_count": 5
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
