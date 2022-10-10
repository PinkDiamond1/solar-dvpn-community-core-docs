## GET `api/nodesByAddress`

---

### Description

This method is used to retrieve list of DVPN nodes by list of their blockchain addresses.

---

### Request body


```
{
    "blockchain_addresses": [
        "sentnode1p7jjqtleeulshm6usegqf4m53xya3eh9vh4d67"
    ]
}
```

| Parameter              | Type        | Description                                                    | Required |
|------------------------|-------------|----------------------------------------------------------------|----------|
| blockchain_addresses[] | [String]    | Array of nodes' blockchain addresses                           | YES      |
| page                   | Int         | Page number                                                    | NO       |

---

### Response

```
{
  "current_page": 1,
  "data": [
    {
      "id": 211,
      "blockchain_address": "sentnode1p7jjqtleeulshm6usegqf4m53xya3eh9vh4d67",
      "is_trusted": true,
      "moniker": "SOLAR dVPN Node #5",
      "remote_url": "https://176.97.68.166:6521",
      "status": "STATUS_ACTIVE",
      "default_price": 1500000,
      "bandwidth_upload": 9480820,
      "bandwidth_download": 11067325,
      "location_country_code": "au",
      "location_continent_code": "oc"
    }
  ],
  "total": 1
}
```

| Parameter                       | Type        | Description                                         |
|---------------------------------|-------------|-----------------------------------------------------|
| current_page                    | Int         | Current results page number                         |
| data[]                          | Array       | Nodes array                                         |
| data[].id                       | Int         | Node ID                                             |
| data[].blockchain_address       | String      | Node blockchain address                             |
| data[].is_trusted               | Bool        | Node trust status (`true` or `false`)               |
| data[].moniker                  | String?     | Node name (aka moniker)                             |
| data[].remote_url               | String      | Node API remote URL                                 |
| data[].status                   | String      | Node status                                         |
| data[].default_price            | Int         | Node price per GB                                   |
| data[].bandwidth_upload         | Int         | Node upload speed                                   |
| data[].bandwidth_download       | Int         | Node download speed                                 |
| data[].location_country_code    | String?     | ISO 3166-2 country code of node                     |
| data[].location_continent_code  | String?     | Two-letter continent code of node                   |
| total                           | Int         | Total elements                                      |

---

### Errors

| Error Message                   |
|---------------------------------|
| UnknownError                    |
