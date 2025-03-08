# Contact API Spec

## Create Contact API

Endpoint : POST /api/contacts

Headers : 
- Autorization : token

Request Body :

```json
{
    "first_name" :"Laila",
    "last_name" : "Qadriyah",
    "email" : "lailaqdr04@gmail.com",
    "phone" : "082171130060"
}
```

Request Body Success :
```json
{
    "data" : {
        "id" : 1,
    "first_name" :"Laila",
    "last_name" : "Qadriyah",
    "email" : "lailaqdr04@gmail.com",
    "phone" : "082171130060"   
    }
}
```

Request Body Error :
```json
{
    "errors" : "Email is not valid format"
}
```

## Update Contact API

Endpoint : PUT /api/contacts/:id

Headers : 
- Autorization : token

Request Body :

```json
{
     "first_name" :"Laila",
    "last_name" : "Qadriyah",
    "email" : "lailaqdr04@gmail.com",
    "phone" : "082171130060"
}
```

Request Body Success :
```json
{
     "data" : {
        "id" : 1,
    "first_name" :"Laila",
    "last_name" : "Qadriyah",
    "email" : "lailaqdr04@gmail.com",
    "phone" : "082171130060"   
    }
}
```

Request Body Error :
```json
{
    "errors" : "Email is not valid format"
}
```

## Get Contact API

Endpoint : GET /api/contacts/:id

Headers : 
- Autorization : token


Request Body Success :
```json
{
    "data" : {
        "id" : 1,
    "first_name" :"Laila",
    "last_name" : "Qadriyah",
    "email" : "lailaqdr04@gmail.com",
    "phone" : "082171130060"   
    }
}
```

Request Body Error :
```json
{
    "errors" : "Contact is not found"
}
```

## Search Contact API

Endpoint : GET /api/contacts

Headers : 
- Autorization : token

Query params :
- name : Search by first_name or last_name, using like, optional
- email : Search by email using like, optional
- phone : Search by phone using like, optional
- page : number of page, default 1
- size : size per page, default 10



Request Body Success :
```json
{
     "data" : [
    {
    "id" : 1,
    "first_name" :"Laila",
    "last_name" : "Qadriyah",
    "email" : "lailaqdr04@gmail.com",
    "phone" : "082171130060"   
    },
    {
    
    "id" : 2,
    "first_name" :"Laila",
    "last_name" : "Qadriyah",
    "email" : "lailaqdr04@gmail.com",
    "phone" : "082171130060"   
    }  
    
     ],
     "paging" : {
        "page" : 1,
        "total_page" : 3,
        "total_item" : 30
     }
}
```

Request Body Error :
```json
{
    
}
```

## Remove Contact API

Endpoint : DELETE /api/contacts/:id

Headers : 
- Autorization : token


Request Body Success :
```json
{
    "data" : "OK"
}
```

Request Body Error :
```json
{
    "errors" : "Contacts is not found"
}
```