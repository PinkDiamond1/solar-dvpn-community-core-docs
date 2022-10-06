## PUT `api/wallet`

---

### Description

This method is used to recover wallet from a seed phrase.

---

### Request


```
{
    "mnemonic": "deer catalog human hint unique grass actual silk poet cupboard process combine fashion exotic eye fork urban entire stable sun blue pistol organ toddler"
}
```

| Parameter                   | Description                                      | Required |
|-----------------------------|--------------------------------------------------|----------|
| mnemonic                    | Seed phrase of the wallet (mnemonic)             | YES      |

---

### Response

```
{
    "address": "sent09uyu0lrfsdvkeop213jsd7fq2rs29krf25ml87",
    "balance": 500000,
    "currency": "udvpn"
}
```

| Parameter                       | Type        | Description                                         |
|---------------------------------|-------------|-----------------------------------------------------|
| address                         | String      | Blockchain address of the wallet                    |
| balance                         | Int         | mount of tokens on the wallet                       |
| currency                        | String      | Currency of the wallet (`udvpn`)                    |

---

### Errors

| Error Message                   |
|---------------------------------|
| UnknownError                    |
