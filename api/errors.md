## About errors

### Description

See more about errors structure [here](https://docs.vapor.codes/basics/errors/).

---

### Error response body

| Parameter     | Type        | Description                                |
|---------------|-------------|--------------------------------------------|
| error         | Bool        | Always `true`                              |
| reason        | String      | Can either be a common `http status` reason, `localizable string` or an `inner error`. See all possible examples below.  |

---

### HTTP error

```
{
    "error": true
    "reason": "Not Found"
}
```
---

### Localizable error

```
{
    "error": true
    "reason": "no_quota_left"
}
```
---

### Inner error

```
{
   "error": true,
   "reason": "{ "message": "RPC timed out before completing", "code": 4 }"
}

```

System (tunnel, network-related, etc), [gRPC errors](https://github.com/grpc/grpc-swift/blob/a0d57279afa61975b8ca0d263f8a19c86bc5c43b/Sources/GRPC/GRPCError.swift) will be passed as is wrapped in a JSON string.

| Parameter     | Type        |
|---------------|-------------|
| message       | String      |
| code          | Int         |
