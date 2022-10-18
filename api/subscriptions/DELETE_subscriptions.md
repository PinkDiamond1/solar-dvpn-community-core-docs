## DELETE `api/subscriptions`
---

### Description
This method is used to unsubscribe from a node.

---
### Request
```
DELETE api/subscriptions?
        node_address=sentnode1p7jjqtleeulshm6usegqf4m53xya3eh9vh4d67
```
| Parameter        | Type        | Required |
|------------------|-------------|----------|
| node_address     | String      | YES      |

---
### Response
200 OK, no response body.

---
### Errors
| Error Code | Error Message               | Description                        |
|------------|-----------------------------|------------------------------------|
| 400        | Decoding error body         |                                    |
| 500        | message from GRPS error     |                                    |
| 404        | Not found                   | No subcription to the node found   |












