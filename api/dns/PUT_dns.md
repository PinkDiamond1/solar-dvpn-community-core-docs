## PUT `api/dns`

---

### Description

This method is used to select a DNS option from available servers.

---

### Request


```
{
    "server": "handshake"
}
```

| Parameter   | Type           | Description                                                | Required |
|-------------|----------------|------------------------------------------------------------|----------|
| server      |  String        | DNS server name from [available options](api/dns/GET_dns_current.md)  | YES      |

---

### Response

200 OK, no response body.

---

### Errors

| Error Code | Reason Phrase      | Description                                       |
|------------|--------------------| --------------------------------------------------|
| 400        | Bad Request        | Unknown server was passed or decoding error       |
