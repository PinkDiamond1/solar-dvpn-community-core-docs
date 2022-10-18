## DELETE `api/connection/sessions`

---

### Description

This method is used to stop all active sessions under current account. This will also result in stoping VPN tunnel if it's active.

---

### Request

No payload required.

---

### Response

200 OK, no response body.

---

### Errors

| Error Code | Error Message                      |
|------------|------------------------------------|
| 500        | "missing_mnemonic"                 |
| 500        | Wrapped GRPC error                 |
