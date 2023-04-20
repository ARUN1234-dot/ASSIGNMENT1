# ASSIGNMENT1
# Prerequisites
For Windows

* Node-gyp (npm install --global node-gyp)
* Express-Validator (npm install --save express-validator)
# Usage
* Run npm install to installl dependencies
* Run npm run start to start the local server
* Load http://localhost:8080 to test the endpoint. It will display a json result {"message":"University of Moratuwa"}
# API Endpoints
# GET /api/customer
Get a list of customer
```json
{ 
  "message": "success",
    "data": [
        {
            "customerId": 1,
            "name": "Karuppan",
            "address": "Lauriston,Bramely,Kandy",
            "email": "arun123@gmail.com",
            "dateOfBirth": "2000.12.25",
            "gender": "male",
            "age": "20",
            "cardHolderName": "Karu",
            "cardNumber": "111125367895",
            "expireDate": "12/2025",
            "cvv": "578",
            "timestamp": "2023-04-20 07:49:49"
        }
    ]
}
```
## GET /api/customer/{id}
Get customer information by product id
```json
{ 
  "message": "success",
    "data": [
        {
            "customerId": 1,
            "name": "Karuppan",
            "address": "Lauriston,Bramely,Kandy",
            "email": "arun123@gmail.com",
            "dateOfBirth": "2000.12.25",
            "gender": "male",
            "age": "20",
            "cardHolderName": "Karu",
            "cardNumber": "111125367895",
            "expireDate": "12/2025",
            "cvv": "578",
            "timestamp": "2023-04-20 07:49:49"
        }
    ]
}
```
## POST /api/customer/
To create a new product based on POST data (x-www-form-url-encoded)
```json
{
            "name": "Karuppan",
            "address": "Lauriston,Bramely,Kandy",
            "email": "arun123@gmail.com",
            "dateOfBirth": "2000.12.25",
            "gender": "male",
            "age": "20",
            "cardHolderName": "Karu",
            "cardNumber": "111125367895",
            "expireDate": "12/2025",
            "cvv": "578",
            "timestamp": ""           
}
```
## PATCH /api/customer/{id}
To update customer data by id, based on POST data (x-www-form-url-encoded)
```json
{
            "name": "Karuppan",
            "address": "Lauriston,Bramely,Kandy",
            "email": "arun123@gmail.com",
            "dateOfBirth": "2000.12.25",
            "gender": "male",
            "age": "20",
            "cardHolderName": "Karu",
            "cardNumber": "111125367895",
            "expireDate": "12/2025",
            "cvv": "578",
            "timestamp": ""           
}
```
## DELETE /api/customer/{id}
To remove a customer from the database by customer id.

This example is using the curl command line

curl -X "DELETE" http://localhost:8080/api/customer/1
The result is:

{"message":"deleted","rows":1}
