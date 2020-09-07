# Easyadds

[![Build Status](https://travis-ci.com/habinezadalvan/Easy-adds.svg?branch=develop)](https://travis-ci.com/habinezadalvan/Easy-adds)
[![Coverage Status](https://coveralls.io/repos/github/habinezadalvan/luxaryapp/badge.svg?branch=develop)](https://coveralls.io/github/habinezadalvan/luxaryapp?branch=develop)

Easy Ads is an online marketplace for selling the stuff you don’t need
anymore. With Easy Ads, users should be able to post stuff such as
Clothing, Cameras, Furniture, Cars, and Phones.


*Getting started with Easyadds apis*

step 1: Clone the repo
step 2: checkout to *Easy-adds*
step 3: use your terminal and run *npm install*
step 4: run *npm run start:dev*, the default port: 5000. The server will be running on http://localhost:5000
step 5: Test api 

  *Endpoints version two (V1) with postgresql database*
  ---------------------------------------------------
  
  | METHOD  | END-POINTS  | DESCRIPTION |
| ------------ |---------------| -----|
| POST     | /api/v1/users/register | signup |
| POST     | /api/V1/users/signin | login |
| POST     | /api/V1/products/product | create product |
| DELETE     | /api/V1/products/product/:id | delete a product |
| GET | /api/V1/products| get all products |
| GET | /api/V1/products/product/:id |    view a single product |
| PUT | /api/V1/products/product/:id  |    update a product |

Addition information: UI features
-------------------------------------
  1. User can sign up.

  2. User can login.

  3. User can create post or create product/stuff.

  4. User can view a specific posted product.

  5. User can view all posted products.

  6. user can delete his/her product.

  7. user can update the stuff.

*API Response Specification*

On success
{
“status”: 200,
“data”: {...}
}
On error
{
“status”: 404,
“error”: “relevant-error-message”
}
Entity Specification
Users
{
“id” : Integer,
“firstName”: String,
“lastName”: String,
“email”: String,
“password”: String,
“address”: String,
“phoneNumber”: String
}
Stuff/Products
{
“id” : Integer,
“ownerId”: Integer, // userId
“title”: String,
“price”: String,
“status”: String, // sold, available
“image”: String,
“categoryId”: Integer, // categoryId
“description”: String
}
Category
{
“id” : Integer,
“name”: String,
“description”: String
}
