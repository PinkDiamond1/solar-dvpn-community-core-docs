## POST `api/wallet`

---

### Description

This method is used to creates brand new wallet and generate new mnemonic.

---

### Request

No payload required.

---

### Response

```
{
   "wallet":{
      "address":"sent09uyu0lrfsdvkeop213jsd7fq2rs29krf25ml87",
      "balance":0,
      "currency":"udvpn"
   },
   "mnemonic": "deer catalog human hint unique grass actual silk poet cupboard process combine fashion exotic eye fork urban entire stable sun blue pistol organ toddler"
}
```

| Parameter                       | Type        | Description                                         |
|---------------------------------|-------------|-----------------------------------------------------|
| wallet                          |             | Wallet Object                                       |
| wallet.address                  | String      | Blockchain address of the wallet                    |
| wallet.balance                  | Int         | Amount of tokens on the wallet                       |
| wallet.currency                 | String      | Currency of the wallet (`udvpn`)                    |
| mnemonic                        | String      | Seed phrase of the wallet (mnemonic)                |

---

### Errors

| Error Code | Reason Phrase           | Description                             |
|------------|-------------------------| ----------------------------------------|
| 401        | missing_mnemonics       | Failed to load mnemonic from keychain   |
| 500        | GRPS messages           | Fetch balance failed                    |
| 500        | Internal server error   |                                         |
