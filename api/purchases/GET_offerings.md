## GET `api/offerings`

---

### Description

This method is used to retreive list of offerings from RevenueCat.  
For more information take a look to RevenueCat documentaion: https://www.revenuecat.com/docs/displaying-products

---

### Request

No payload required.

---

### Response

```
[
   {
      "serverDescription":"DVPN packages",
      "availablePackages":[
         {
            "storeProduct":{
               "price":1.05,
               "currency":"€"
            },
            "offeringIdentifier":"community_dvpn",
            "localizedPriceString":"1,05 €",
            "packageType":-1,
            "identifier":"dvpn_100"
         },
         {
            "storeProduct":{
               "price":2.05,
               "currency":"€"
            },
            "offeringIdentifier":"community_dvpn",
            "localizedPriceString":"2,05 €",
            "packageType":-1,
            "identifier":"dvpn_500"
         }
      ],
      "identifier":"community_dvpn"
   }
]
```

Offering model

| Parameter         | Type        | Description                                                           |
|-------------------|-------------|-----------------------------------------------------------------------|
| identifier        | String      |  Unique identifier defined in RevenueCat dashboard                    |
| serverDescription | String      |  Offering description defined in RevenueCat dashboard                 |
| availablePackages | [Package]   |  Array of `Package` objects available for purchase                    |
| lifetime          | Package?    |  Lifetime `Package` type configured in the RevenueCat dashboard       |
| annual            | Package?    |  Annual `Package` type configured in the RevenueCat dashboard         |
| sixMonth          | Package?    |  Six month `Package` type configured in the RevenueCat dashboard      |
| threeMonth        | Package?    |  Three month `Package` type configured in the RevenueCat dashboard    |
| twoMonth          | Package?    |  Two month `Package` type configured in the RevenueCat dashboard      |
| monthly           | Package?    |  Monthly `Package` type configured in the RevenueCat dashboard        |
| weekly            | Package?    |  Weekly `Package` type configured in the RevenueCat dashboard         |

Package model

| Parameter                          | Type         | Description                                                     |
|------------------------------------|--------------|-----------------------------------------------------------------|
| identifier                         | String       |  The identifier for this Package                                |
| packageType                        | Int          |  The type configured for this package                           |
| storeProduct                       | StoreProduct |  The underlying `StoreProduct`                                  |
| offeringIdentifier                 | String       |  The identifier of the `Offering` containing this Package       |
| localizedPriceString               | String       |  The formatted price of this product                            |

StoreProduct model

| Parameter             | Type        | Description                      |
|-----------------------|-------------|----------------------------------|
| price                 | Decimal     |  The price of this product       |
| currency              | String      |  Currency symbol                 |

PackageType

| Value       | Type        |
|-------------|-------------|
| -2          | unknown     |
| -1          | custom      |
| 0           | lifetime    |
| 1           | annual      |
| 2           | sixMonth    |
| 3           | threeMonth  |
| 4           | twoMonth    |
| 5           | monthly     |
| 6           | weekly      |

---

### Errors

| Error Code | Error Message               | Description                                |
|------------|-----------------------------|--------------------------------------------|
| 500        | Some RevenueCat messages    |                                            |
