# Address API Spec

## Create Address API

Endpoint : POST /api/contacts/:contactId/address

Headers :

- Authorization : token

Request Body :

```json
{
  "street": "Jl. Jalan",
  "city": "Nunukan",
  "province": "Kalimantan Utara",
  "country": "Indonesia",
  "postalCode": "999999"
}
```

Response Body Success:

```json
{
  "data": {
    "id": 1,
    "street": "Jl. Jalan",
    "city": "Nunukan",
    "province": "Kalimantan Utara",
    "country": "Indonesia",
    "postalCode": "999999"
  }
}
```

Response Body Error :

```json
{
  "errors": "country is required"
}
```

## Update Address API

Endpoint : PUT /api/contacts/:contactId/address/:addressId

Headers :

- Authorization : token

Request Body :

```json
{
  "street": "Jl. Jalan",
  "city": "Nunukan",
  "province": "Kalimantan Utara",
  "country": "Indonesia",
  "postalCode": "999999"
}
```

Response Body Success:

```json
{
  "data": {
    "id": 1,
    "street": "Jl. Jalan",
    "city": "Nunukan",
    "province": "Kalimantan Utara",
    "country": "Indonesia",
    "postalCode": "999999"
  }
}
```

Response Body Error :

```json
{
  "errors": "country is required"
}
```

## Get Address API

Endpoint : GET /api/contacts/:contactId/address/:addressId

Headers :

- Authorization : token

Response Body Success:

```json
{
  "data": {
    "id": 1,
    "street": "Jl. Jalan",
    "city": "Nunukan",
    "province": "Kalimantan Utara",
    "country": "Indonesia",
    "postalCode": "999999"
  }
}
```

Response Body Error :

```json
{
  "errors": "contact not found"
}
```

## List Address API

Endpoint : GET /api/contacts/:contactId/address

Headers :

- Authorization : token
  cc
  Response Body Success:

```json
{
  "data": [
    {
      "id": 1,
      "street": "Jl. Jalan",
      "city": "Nunukan",
      "province": "Kalimantan Utara",
      "country": "Indonesia",
      "postalCode": "999999"
    },
    {
      "id": 2,
      "street": "Jl. Aspal",
      "city": "Nunukan",
      "province": "Kalimantan Utara",
      "country": "Indonesia",
      "postalCode": "999989"
    }
  ]
}
```

Response Body Error :

```json
{
  "errors": "contact not found"
}
```

## Remove Address API

Endpoint : DELETE /api/contacts/:contactId/address/:addressId

Headers :

- Authorization : token

Response Body Success:

```json
{
  "data": "OK"
}
```

Response Body Error :

```json
{
  "errors": "contact not found"
}
```
