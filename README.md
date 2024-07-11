# Cash Card Application

The chart below has more details about RESTful CRUD operations.

| Operation | API Endpoint     | HTTP Method | Response Status   |
|-----------|------------------|-------------|-------------------|
| Create    | /cashcards       | POST        | 201 (CREATED)     |
| Read      | /cashcards/{id}  | GET         | 200 (OK)          |
| Update    | /cashcards/{id}  | PUT         | 204 (NO CONTENT)  |
| Delete    | /cashcards/{id}  | DELETE      | 204 (NO CONTENT)  |

### The GET Request Contract
**Request**

- URI: `/cashcards/{id}`
- HTTP Verb: GET
- Body: None

**Response**

- HTTP Status:
  - `200 OK` if the user is authorized and the Cash Card was successfully retrieved
  - `401 UNAUTHORIZED` if the user is unauthenticated or unauthorized
  - `404 NOT FOUND` if the user is authenticated and authorized but the Cash Card cannot be found
- Response Body Type: JSON
- Example Response Body:
  ```json
  {
    "id": 99,
    "amount": 123.45
  }

### The POST Request Contract

**Request**

- URI: `/cashcards`
- HTTP Verb: POST
- Body:
```json
  {
    "amount": 123.45
  }
```
**Response**
- Status Code: `201 CREATED` 
- Header: `Location=/cashcards/42`