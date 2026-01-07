# Contact API Spec

## Create Contact API

Endpoint : POST /api/contacts

Headers : 
- Authorization : token

Request Body : 
```json
{
    "firstName" : "Yusuf",
    "lastName" : "Sidik",
    "email" : "email@gmail.com",
    "phone" : "02121212121"
}
```
Response Body Success : 
```json
{
    "data" : {
        "id": 1,
        "firstName" : "Yusuf",
        "lastName" : "Sidik",
        "email" : "email@gmail.com",
        "phone" : "02121212121"
    },
}
```

Response Body Error : 

```json
{
    "errors" : "Email is not valid format"
}
```
## Update Contact API
Endpoint : PUT /api/contacts/:id

Headers : 
- Authorization : token

Request Body : 
```json
{
    "firstName" : "Yusuf",
    "lastName" : "Sidik",
    "email" : "email@gmail.com",
    "phone" : "02121212121"
}
```
Response Body Success : 
```json
{
    "data" : {
        "id": 1,
        "firstName" : "Yusuf",
        "lastName" : "Sidik",
        "email" : "email@gmail.com",
        "phone" : "02121212121"
    },
}
```

Response Body Error : 

```json
{
    "errors" : "Email is not valid format"
}
```

## Get Contact API
Endpoint : GET /api/contacts/:id

Headers : 
- Authorization : token

Response Body Success : 
```json
{
    "data" : {
        "id": 1,
        "firstName" : "Yusuf",
        "lastName" : "Sidik",
        "email" : "email@gmail.com",
        "phone" : "02121212121"
    },
}
```

Response Body Error : 

```json
{
    "errors" : "Contact not found"
}
```

## Search Contact API
Endpoint : GET /api/contacts

Headers : 
- Authorization : token

Query Params : 
- name : Search by firstName or lastName, using LIKE query, optional
- email : Search by email, using LIKE, optional
- phone : Search by phone , using LIKE, optional
- page : number of page, default 1
- size : size per page, default 10

Response Body Success : 
```json
{
    "data" : [
        {
            "id": 1,
            "firstName" : "Yusuf",
            "lastName" : "Sidik",
            "email" : "email@gmail.com",
            "phone" : "02121212121"
        },
        {
            "id": 2,
            "firstName" : "Kholid",
            "lastName" : "Yusuf",
            "email" : "email@gmail.com",
            "phone" : "02121444121"
        },
    ],
    "paging" : {
        "page" : 1,
        "totalPage" : 3,
        "totalItem" : 30
    }
}
```

Response Body Error : 

```json
{
    "errors" : ""
}
```

## Remove Contact API
Endpoint : DELETE /api/contacts/:id

Headers : 
- Authorization : token

Response Body Success : 
```json
{
    "data" : "OK",
}
```

Response Body Error : 

```json
{
    "errors" : "Contact not found"
}
```
