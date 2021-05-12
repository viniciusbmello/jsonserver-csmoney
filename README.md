# CS Money
This repository contains a simple API for the [CS Money](https://csmoney.herokuapp.com/) front-end challenge.
Requirements:
* [NodeJS v5.2.0+](https://nodejs.org/en/download/)

## How to run
Clone/Download this repository, run `npm install` and` npx json-server db.json`. The API is located at `http: // localhost: 3000`.

## Routes
All POST requests for this API must contain the `Content-Type: application / json` header.
This API contains the following routes:

* `GET /transaction`: lists the registered transaction
* `POST /transaction`: create a new transaction
* `DELETE /transaction /: id`: delete the transaction with ID: id

## Examples

### GET /transaction

Request: 
```javascript
GET /transaction
```
Response:
```javascript
[
  {
    "id": 1,
    "title": "Freelance RocketSeat",
    "type": "deposit",
    "category": "Dev",
    "amount": 2000,
    "createdAt": "2021-05-08T03:35:31.860Z"
  },
  {
    "id": 2,
    "title": "House Rent",
    "type": "withdraw",
    "category": "Bills",
    "amount": 900,
    "createdAt": "2021-05-04T05:25:41.430Z"
  }
]
```

### POST /transaction

Request: 
```javascript
// POST /transaction
// Content-Type: application/json
{
    "title": "Supermarket",
    "type": "withdraw",
    "category": "Bills",
    "amount": 300,
    "createdAt": "2021-05-09T09:25:41.490Z"
}
```

Response:
```javascript
{
    "title": "Supermarket",
    "type": "withdraw",
    "category": "Bills",
    "amount": 300,
    "createdAt": "2021-05-09T09:25:41.490Z",
    "id": 3
}
```

### DELETE /transaction/:id
Request:
```javascript
DELETE /transaction/3
```

Response:
```javascript
// Status: 200 OK
{}
```
