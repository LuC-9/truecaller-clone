# truecaller-clone || DJANGO TRUECALLER
A phonebook API written in Django REST framework.

Steps to run the API
## Install dependencies
```
pip3 install requirements.txt
```

## Runserver
```
python3 manage.py runserver
```
## Test the API
```
Route: http://localhost:8000/account/register
Request Type: POST
Data: 

    {
        "name":"LuC",
        "password":"123abc",
        "phone_number":"77778787887",
        "email":"abc@gmail.com",
    }
```

```
Route: http://localhost:8000/account/login/
Request Type: POST
Data: 

    {
        "username":"LuC",
        "password":"123abc"
    }
```
### JWT AUTH
You will receive a JWT Auth Token after signUp and signIn.
Include the JWT token in headers as a Bearer Token for all private requests
```
Authorization: token eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpZCI6MSwidXNlcm5hbWUiOiJhbmt1ciJ9.eQicFQy2nYric9Gl2mhqOH4l8An7B_Kf2CKoJmZrPcA
```

### To view all the contacts
```
Public Route: http://localhost:8000/account/contacts/
Request Type: GET
```

### To mark a contact as SPAM
```
Private Route: http://localhost:8000/account/spams/
Request Type: POST
Data:
    {
        "phone": "9773661768"
    }
```

### To search a contact by name
```
Private Route: http://localhost:8000/account/search_by_name?name=Chhaya
Request Type: GET
```
or 
```
Private Route: http://localhost:8000/account/search_by_name/
Data:
    {
        "name":"Chhaya"
    }
Request type: GET
```

### To search a contact by phone
```
Private Route: http://localhost:8000/account/search_by_phone_number?phone_number=8510978234
Request Type: GET
```
or
```
Private Route: http://localhost:8000/account/search_by_phone_number/
Data:
    {
        "phone_number"=8510978234
    }
Request Type: GET
```
FIND THE SCREENSHOTS OF THE API CALLS IN THE POSTMAN SCREENSHOTS FOLDER
