## POST `api/purchase`

---

### Description

This method is used to purchase a product in RevenueCat.  
For more information take a look to RevenueCat documentaion: https://www.revenuecat.com/docs/displaying-products

---

### Request

```
{
    "package_identifier":"dvpn_100"
}
 ```

| Parameter           | Type        | Description                                |
|---------------------|-------------|--------------------------------------------|
| package_identifier  | String      |  Identifier of package                     |

---

### Response

```
200 OK, no response body.
```

---

### Errors

| Error Code | Error Message               | Description                                |
|------------|-----------------------------|--------------------------------------------|
| 500        | Some RevenueCat messages    |                                            |
| 404        | Not found                   | No package with `package_identifier` found |
