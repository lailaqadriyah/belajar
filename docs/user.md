# User API Spec

## Register User API

Endpoint : POST /api/users

Request Body :

```json
{
    "username" : "pzn",
    "password" : "rahasia",
    "name" : "Programmer Zaman Now"
}
```

Response Body Succes :
```json
{

    "data" : {
    "username" : "pzn",
    "name" : "Programmer Zaman Now"
    }
    
}
```

Response Body Error :

```json
{
    "errors" : "Username already registered"
}
```

## Login User API

Endpoint : POST /api/users/login

Request Body :

```json
{
    "username" : "pzn",
    "password" : "rahasia"
}
```

Response Body Succes :

```json
{
    "data" :{
        "token" : "unique-token"
    }
}
```
Response Body Error :

```json
{
    "errors" : "Username or password wrong"
}
```

## Update User API

Endpoint : PATCH /api/users/current

Headers : 
- Autorization : token

Request Body:

```json
{
    "name" : "Programmer Zaman Now Lagi", //optional
    "password" : "new password" //optional
}
```

Response Body Success :

```json
{
    "data" : {
        "username" :"pzn",
        "name" : "Programmer Zaman Now"
    }
}
```
Response Body Error :

```json
{
    "errors" : "Name length max 100"
}
```

## Get User API

Endpoint : GET /api/users

Headers :
- Autorization : token

Response Body Success:
```json
{
    "data" : {
        "username" : "pzn",
        "name" : "Programmer Zaman Now"
    }
}
```

Response Body Error :

```json
{
    "errors" : "Unautorized"
}
```

## Logout User API

Endpoint : DELETE /api/users/logout

Headers :
- Autorization : token

Response Body Success:

```json
{
    "data" : "OK"
}
```

Response Body Error :

```json
{
    "errors" : "Unautorized"
}
```