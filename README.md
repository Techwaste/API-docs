
# api documentation v0.0.2

yahoo~! How are ya? I hope you guys doing well, and hopefully find love among this cruel world! Because as an old wise man once said: 

"**one would most be thought to love a person if one wishes that he should exist, for his sake and not one's own, even if one doesn't confer goods on him, let alone existence**."   
-Aristotle

what about me you may ask!?
my reaction to that question :  
![me frfr](https://media.tenor.com/6sC2tvkCiU0AAAAC/micha%C5%82-micha%C5%82po-nesquicku.gif)

anyways due to some technical issues (my brain and my low iq), I managed to fix the api and here's the updated version of the documentation:
### REGISTER

- URL
    
    /user/signup
    
- METHOD
    
    POST
    
- REQUEST BODY
```json
{
  "fullname": "string",
  "email": "user@example.com",
  "password": "string"
}
  ```  
- RESPONSE
    
```json
{
  "error": "false",
  "message": "User Created",
  "signupToken": {
    "access token": "aAiOiJfadsfdsafdsfKV1sadfQiLCfasdfdsaIUzIasdasdas32834hwytg90uerqhy908354nhg08erqh08q35nh0ierfh-ber-q9jh-945-0sdfjhme-tonjet9-tjn9-j-9j54h0-9nmeri0fhnbm-09rnobjknfds0ibn03n"
  }
}
```
    

### LOGIN

- URL
    
    /user/login
    
- METHOD
    
    POST
    
- REQUEST BODY
    
```json
{
  "email": "user@example.com",
  "password": "string"
}
```
    
- RESPONSE
```json
{
  "error": "false",
  "message": "login success",
  "loginResult": {
    "userId": {
      "id": 3,
      "Username": "gabrieltest3"
    },
    "token": {
      "access token": "eyJ0eXAiOiJKV1QiLCJhbGdF0TCem7fhAK57fIPyM3K9VI2I"
    }
  }
```
    

### PREDICT

- URL
    
    /predict
    
- METHOD
    
    POST
    
- HEADERS
    
    Content-Type: multipart/form-data
    
    Authorization: Bearer <Token>
    
- REQUEST BODY
    
    photo as file **`Image must be jpg, jpeg, or png format!`**
    
- RESPONSE
    
```json
{
  "compID": 2,
  "cable": 28.659623861312866
}
```
    

### COMPONENT

- URL
    
    /component{id}
    
- METHOD
    
    GET{id}
    
- HEADERS
    
    Authorization: Bearer <Token>
    
- PARAMETERS
name * = string
    
- RESPONSE
    
```json
{
  "error": "false",
  "message": "success",
  "componentList": {
    "id": 1,
    "name": "battery",
    "desc": "A battery consists of one or more electrochemical cells that contains chemical energy and release it as electrical energy. Batteries are generally safe if being used properly. The most common danger associated with batteries if mishandled or damaged is explosion or fire.",
    "example": "https://www.canford.co.uk/Images/ItemImages/large/59-104_01.jpg"
  }
}
```
    

### ARTICLE

- URL
    
    /article{id}
    
- METHOD
    
    GET{id}
    
- HEADERS
    
    Authorization: Bearer <Token>
    
- REQUEST BODY
    
    component id as STRING (foreign key from result-id)
    
- RESPONSE
    
```json
{
  "error": "false",
  "message": "success",
  "articleList": [
    {
      "id": 2,
      "name": "test3",
      "desc": "testing",
      "articleImageURL": "testing.test",
      "componentId": 3
    }
  ]
}
```
### Get All Article
- URL
    
    /allArticle
    
- METHOD
    
    GET
    
- HEADERS
    
    Authorization: Bearer <Token>
    
   
- RESPONSE
```json
{
  "error": "false",
  "message": "success",
  "componentList": [
    {
      "id": 6,
      "name": "nomer satu",
      "desc": "nomerSatu",
      "articleImageURL": "testing.test",
      "componentId": 1
    },
    {
      "id": 5,
      "name": "nomer satu",
      "desc": "nomerSatu",
      "articleImageURL": "testing.test",
      "componentId": 2
    },
    {
      "id": 4,
      "name": "nomer satu",
      "desc": "nomerSatu",
      "articleImageURL": "testing.test",
      "componentId": 2
    },
    {
      "id": 3,
      "name": "nomer satu",
      "desc": "nomerSatu",
      "articleImageURL": "testing.test",
      "componentId": 1
    },
    {
      "id": 2,
      "name": "test3",
      "desc": "testing",
      "articleImageURL": "testing.test",
      "componentId": 3
    },
    {
      "id": 1,
      "name": "test",
      "desc": "testing",
      "articleImageURL": "testing.test",
      "componentId": 1
    }
  ]
}
```
