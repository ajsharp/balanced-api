# Bank Account

## Get a bank account

    GET /:version/bank_accounts/:bank_account_id

### Response

#### Header

    Status: 200 OK

#### Body

```javascript
{
    "id": "BANm9b8BcoOjcF5i1p4eV9I",
    "name": "Gottfried Leibniz",
    "account_number": "xxxxxx2930",
    "routing_number": "121042882",
    "type": "checking"
}
```


## Create a bank account

    POST /:version/bank_accounts

### Request

`name`
: **string** or _null_
: **default** _null_

`account_number`
: _required_ **string**

`routing_number`
: _required_ **string**

`type`
: _required_ **string**
: `checking` or `savings`

```javascript
{
    "name": "Gottfried Leibniz",
    "account_number": "3819372930",
    "routing_number": "121042882",
    "type": "checking"
}
```

### Response

#### Header

    Status: 201 Created

#### Body

```javascript
{
    "id": "BANm9b8BcoOjcF5i1p4eV9I",
    "name": "Gottfried Leibniz",
    "account_number": "xxxxxx2930",
    "routing_number": "121042882",
    "type": "checking"
}
```


## Delete a bank account

    DELETE /:version/bank_accounts/:bank_account_id

### Response

#### Header

    Status: 204 No Content