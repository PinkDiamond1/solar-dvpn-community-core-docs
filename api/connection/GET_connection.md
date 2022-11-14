## GET `api/connection`

---

### Description

This method is used to get current node address and connection status.

---

### Request

No payload required.

---

### Response

```
{
    "nodeAddress": "sentnode1p7jjqtleeulshm6usegqf4m53xya3eh9vh4d67",
    "tunnelStatus": "disconnected"
}
```

| Parameter    | Type        | Description                                    |
|--------------|-------------|------------------------------------------------|
| nodeAddress  | String      | Node blockchain address                        |
| tunnelStatus | String      | `connected` or `disconnected`                  |

---

### Errors

No possible errors.
