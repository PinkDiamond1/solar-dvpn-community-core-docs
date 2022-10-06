## GET `api/dns/list`

---

### Description

This method is used to retrieve available DNS options.

---

### Request

No payload required.

---

### Response

```
{
   "servers" : [
    {
      "name": "handshake"
      "addresses": "103.196.38.38, 103.196.38.39"
    }
   ]
}
```

| Parameter              | Type        | Description                  |
|------------------------|-------------|------------------------------|
| servers[]              | Array       | DNS servers array            |
| servers[].name         | String      | Name of the DNS server       |
| servers[].addresses    | String      | DNS server addresses         |

---

### Errors

No possible errors.
