---
layout: page
title: Users
permalink: /users/
---

<h3>Methods</h3>
* [Register](#register)
* [Login](#login)

<br/>

<h4 id="register">Register</h4>
HTTP Method: POST
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/user/register

Payload Example
<pre>
{
  "username": "apiguy",
  "email": "apiguy@eddmi.com",
  "phone": "919076347",
  "gender": "M",
  "password": "apiguy"
}
</pre>


Response Example
<pre>
{
  "code": 201,
  "status": "Created",
  "message": "User created with success",
  "data": {
    "id": "10",
    "facebook_id": null,
    "username": "apiguy",
    "email": "apiguy@eddmi.com",
    "phone": "919076347",
    "gender": "M",
    "birth_date": null,
    "token": "2641e362502c40d055844c42a0ca77b6",
    "image": null,
    "cover_image": null,
    "is_public": 1,
    "is_push_active": 1,
    "logged": 0,
    "app_share": null,
    "points_to_assign": "0"
  }
}
</pre>
<br/>


<h4 id="login">Login</h4>
HTTP Method: POST
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/user/login

Payload Example
<pre>
{
  "email": "apiguy@eddmi.com",
  "password": "apiguy"
}
</pre>

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "User logged with success",
  "data": {
    "id": "10",
    "facebook_id": null,
    "username": "apiguy",
    "email": "apiguy@eddmi.com",
    "phone": "919076347",
    "gender": "M",
    "token": "c122c43f13d2b9662e810e52bf7406e6",
    "image": null,
    "cover_image": null,
    "is_public": "1",
    "is_push_active": "1",
    "logged": 1,
    "app_share": null,
    "points_to_assign": "0",
    "is_followed": 0,
    "follows": {
      "users": 0,
      "brands": 0,
      "products": 0
    },
    "comments": 0,
    "wishlists": 0,
    "points": []
  }
}
</pre>
<br/>
