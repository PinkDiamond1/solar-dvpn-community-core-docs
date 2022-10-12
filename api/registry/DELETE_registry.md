## DELETE `api/registry`

---

### Description

This method is used to delete a specific value from local key-value registry.

---

### Request

```
DELETE api/registry?
        key=foo
```

| Parameter        | Type        | Required |
|------------------|-------------|----------|
| key              | String      | YES       |

---

### Response

200 OK, no reponse body.

---

### Errors

| Error Code | Reason Phrase      | Description                             |
|------------|--------------------| ----------------------------------------|
| 400        | Bad Request        | Decoding error                          |
| 401        | Unauthorized       | Secure registry is unaccessable         |
