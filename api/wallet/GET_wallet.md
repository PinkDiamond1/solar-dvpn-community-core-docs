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
   "address":"sent09uyu0lrfsdvkeop213jsd7fq2rs29krf25ml87",
   "balance":0,
   "currency":"udvpn"
}
```

| Parameter                       | Type        | Description                                         |
|---------------------------------|-------------|-----------------------------------------------------|
| address                         | String      | Blockchain address of the wallet                    |
| balance                         | Int         | Amount of tokens on the wallet                       |
| currency                        | String      | Currency of the wallet (`udvpn`)                    |

---

### Errors

| Error Code | Reason Phrase           | Description                             |
|------------|-------------------------| ----------------------------------------|
| 500        | GRPS messages           | Fetch balance failed                    |
| 500        | Internal server error   |                                         |
