## POST `api/registry`

---

### Description

This method is used to set specific value. Overrides, if exists. 

---

### Request

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

### Response

200 OK, no response body.

---

### Errors

| Error Code | Reason Phrase                 | Description                             |
|------------|-------------------------------| ----------------------------------------|
| 401        | Unauthorized                  | Secure registry is unaccessable         |
| 500        | Internal Server Error         |                                         |
