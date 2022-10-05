## GET `api/wallet`

---

### Description

This method is used to retrieve wallet information.

---

### Request

No payload required.

---

### Response

```
{
   "address":"sent1plmslu3khrux7ycpfvcyjlpy9vxczzhxmjr7za",
   "balance":0,
   "currency":"udvpn"
}
```

| Parameter                       | Type        | Description                                         |
|---------------------------------|-------------|-----------------------------------------------------|
| address                         | String      | Sentinel blockchain address for user's wallet       |
| balance                         | Int         | Amount of tokens in current currency                |
| currency                        | String      | Currency (`udvpn`)                                  |

---

### Errors

| Error Message                   |
|---------------------------------|
| UnknownError                    |
