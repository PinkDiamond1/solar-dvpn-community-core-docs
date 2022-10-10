## GET `api/subscriptions/{node_address}`

---

### Description

This method is used to get quota for a specific node.

---

### Request


```
GET api/subscriptions/sentnode1p7jjqtleeulshm6usegqf4m53xya3eh9vh4d67
```

---

### Response

```
{
   "address": sent...dvrg,
   "consumed": "75000000",
   "allocated": "1000000000"
}
```

| Parameter                       | Type        | Description                                         |
|---------------------------------|-------------|-----------------------------------------------------|
| address                         | String      | Wallet-subscription owner  blockchain address       |
| consumed                        | String      | Consumed bandwidth                                  |
| allocated                       | String      | Allocated bandwidth                                 |                    


---

### Errors

| Error Code | Error Message               | Description                        |
|------------|-----------------------------|------------------------------------|
| 400        | Decoding error body         |                                    |
| 500        | message from GRPS error     |                                    |
| 404        | Not Found                   | Subscription to a node not found   |
