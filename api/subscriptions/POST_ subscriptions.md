## POST `api/subscriptions`

---

### Description

This method is used to subscribe to a node (buy data allowance).

---

### Request


```
{
    "node_address": "sentnode1p7jjqtleeulshm6usegqf4m53xya3eh9vh4d67",
    "amount": "101",
    "currency": "udvpn"
}
```

| Parameter     | Type        | Description                                |
|---------------|-------------|--------------------------------------------|
| node_address  | String      | Node's blockchain address                  |
| amount        | String      | Amount of money to broadcust to the node   |
| currency      | String      | Currency of the wallet (`udvpn`)           |


---

### Response

200 OK, no response body.

---

### Errors

| Error Code | Error Message               | Description                        |
|------------|-----------------------------|------------------------------------|
| 400        | Decoding error body         |                                    |
| 401        | message from GRPS error     |                                    |
| 402        | -                           | Not enought tokens to subscribe    |
