# api documentation v0.0.1

BEHOLD! Our API documentation!  
hopefully this could be a great references for us  
![me moment](https://media.tenor.com/__Bp2a09mF8AAAAM/cr1tikal-penguinz0.gif)

### REGISTER

- URL
    
    /register
    
- METHOD
    
    POST
    
- REQUEST BODY
    
    name as STRING
    
    email as STRING
    
    password as STRING
    
- RESPONSE
    
      {
       "error": false,
        "message": "User Created"
      }
    

### LOGIN

- URL
    
    /login
    
- METHOD
    
    POST
    
- REQUEST BODY
    
    email as STRING
    
    password as STRING
    
- RESPONSE
    
      {
    
      “error”: false,
    
      “message”: “login success”,
    
      “loginResult” : {
    
        “userId”: “user-135u29ht9084h32gt”
    
        “name”: “arip”,
    
        “token”: “sadg834hg03hw0ndsof0dhssadgf43gdsrgf34gdsa08gh240edasjkf9fdjg09dsfjg43294”
    
                      }
    
      }
    

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
    
      {
        "error": false,
        "message": "success"
    
        “predictResult”:{ 
    
          result : “phone: 90.349859384”
    
          resultId: “1”
    
        }
    
      }
    

### COMPONENT

- URL
    
    /component
    
- METHOD
    
    GET{id}
    
- HEADERS
    
    Authorization: Bearer <Token>
    
- REQUEST BODY
    
    component id as STRING (foreign key from result-id)
    
- RESPONSE
    
        {
          "error": false,
          "message": "success"
    
          “componentList”: [
    
        {
    
          “id”:”23”,
    
          “nama”:”keycaps”,
    
          “description”:”anunya keyboard”
    
          “imageExample”:”https://gsutil/sebuahember/contoh1.jpg”
    
        }
    
        ]
    
        }
    

### ARTICLE

- URL
    
    /article
    
- METHOD
    
    GET{id}
    
- HEADERS
    
    Authorization: Bearer <Token>
    
- REQUEST BODY
    
    component id as STRING (foreign key from result-id)
    
- RESPONSE
    
        {
          "error": false,
          "message": "success"
    
          “articleList”: [
    
        {
    
          “idArticle”:”1”,
    
          “nama”:”tahukah kamu? menelan keyboard bisa jadi…”
    
          “description”:”keyboard ternyata bisa jadi.. 🤯”
    
         “articlePhotoUrl”:”https://gsutil/sebuahember/contoh1.jpg”
    
       }
    
                    ]
    
      }
