## POST `api/connection`

---

### Description

This method is used to create a connection to the specific node.

---

### Request

```
{
    "node_address": "sentnode1p7jjqtleeulshm6usegqf4m53xya3eh9vh4d67"
}
```

| Parameter          | Type        | Description                     | Required |
|--------------------|-------------|---------------------------------|----------|
| node_address       | String      | Node's blockchain address       | YES      |

---

### Response

202 Accepted, empty body

---

### Errors

| Error Code | Reason Phrase                       |
|------------|-------------------------------------|
| 500        | Unknown Error                       |
| 500        | Already Connected                   |

### WebSocket Events
Since fetching connection info and creating a tunnel is a time-consuming operation 
all related events and error will be transmitted to the client over the WebSocket connection.

Wallet-related errors
            
| Error Code | Error Message               |
|------------|-----------------------------|
| 403        | accountMatchesDestination   |
| 401        | missingMnemonics            |
| 401        | missingAuthorization        |
| 401        | mnemonicsDoNotMatch         |
| 402        | notEnoughTokens             |
| 500        | savingError                 |
| 500        | signatureGenerationFailed   |
| 500        | balanceUpdateFailed         |

Node-related errors
| Error Code | Error Message               |
|------------|-----------------------------|
| 500        | GRPS messages               |
| 500        | nodeIsOffline               |
| 404        | noSubscription              |
| 401        | noQuotaLeft                 |

Tunnel-related errors
| Error Code | Error Message                       |
|------------|-------------------------------------|
| 500        | Some system messages                |
| 500        | tunnelIsAlreadyActive               |
