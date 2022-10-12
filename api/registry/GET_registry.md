## GET `api/registry`

---

### Description

This method is used to retrieve a specific value from local key-value registry.

---

### Request

```
GET api/registry?
    key=foo
```

| Parameter        | Type        | Required |
|------------------|-------------|----------|
| key              | String      | YES       |

---

### Response

```
{
    “key”: “foo”
    “value”: “bar”,
    “is_secure”: true
}
```

| Parameter    | Type        | Description                          |
|--------------|-------------|--------------------------------------|
| key          | String      | Name                                 |
| value        | String      | Content to be put in registry        |
| is_secure    | Bool        | Specifies which reqistry to use      |

---

### Errors

| Error Code | Reason Phrase      | Description                                       |
|------------|--------------------| --------------------------------------------------|
| 400        | Bad Request        | Decoding error                                    |
| 404        | Not Found          | No value found in any registry by provided key    |
