## GET `api/dns/current`

---

### Description

This method is used to retrieve selected DNS option.

---

### Request

No payload required.

---

### Response

```
{
   "name": "handshake"
   "addresses": "103.196.38.38, 103.196.38.39"
}
```

| Parameter           | Type        | Description                  |
|---------------------|-------------|------------------------------|
| name                | String      | Name of the DNS server       |
| addresses           | String      | DNS server addresses         |

---

### Errors

No possible errors.
