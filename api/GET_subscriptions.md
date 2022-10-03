## GET `api/subscriptions`

---

### Description

This method is used to retrieve list of addresses of nodes user is subscribed to.

---

### Request


```
No payload required.
```

---

### Response

```
{
   "data":[
      "sentnode1p7jjqtleeulshm6usegqf4m53xya3eh9vh4d67"
   ]
}
```

| Parameter                       | Type        | Description                                         |
|---------------------------------|-------------|-----------------------------------------------------|
| data[]                          | [String]    | Array of nodes addresses                            |


---

### Errors

| Error Message                   |
|---------------------------------|
| UnknownError                    |
