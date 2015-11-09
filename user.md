---
layout: page
title: Users
permalink: /users/
---
<p>Allowed operations for brands. Note that authentication is required for some endpoints.</p>
<br/>

<h3>Methods</h3>
[Register](#register) | 
[Login](#login) | 
[Facebook Login](#fblogin) | 
[Get User](#get) | 
[Update User](#update) | 
[Get User Comments](#comments) | 
[Get User Wishlists](#wishlists) | 
[Get User Points](#points) | 
[Get User Followers](#followers) | 
[Follow User](#follow) | 
[Unfollow User](#unfollow) | 
[Update User Images](#images)

<br/>
<br/>
<br/>

<h4 id="register">Register</h4>
HTTP Method: POST
<br/>
Requires Authentication: x
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/user/register](http://wizzyshop.eddmi.com/api/user/register)

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
Requires Authentication: x
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/user/login](http://wizzyshop.eddmi.com/api/user/login)

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


<h4 id="fblogin">Facebook Login</h4>
HTTP Method: POST
<br/>
Requires Authentication: x
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/user/login_fb](http://wizzyshop.eddmi.com/api/user/login_fb)

Payload Example
<pre>
{
    "fb_token": "CAALnXgSvbZCQBAEPRjkGWjMyHvUS5PIY7UfWHzgB6Y01X4xEjoZAB7sL8urEeo7KVZBUznALBKDnIcegArC67tnVKkHUHf7lRD4xG4wSioDybkvwmQejBRjr5Qfrti8mpidcBSv9Agen4fqB5g84ss58cZADwHf6pq2mc5pWD76smieJuiJGxTeZBQ45JD58el9eWQUdgeIgma78JGlem"
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
    "facebook_id": 112994649040578,
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


<h4 id="get">Get User</h4>
HTTP Method: GET
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/user](http://wizzyshop.eddmi.com/api/user)

Response Example if Self
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "User data retrieved with success",
  "data": {
    "id": "3",
    "facebook_id": null,
    "username": "apiguy",
    "email": "apiguy@eddmi.com",
    "phone": "919072344",
    "gender": "M",
    "token": "8db67e9a8c1744ed1b0226a91894da05",
    "image": null,
    "cover_image": null,
    "is_public": "1",
    "is_push_active": "1",
    "logged": "0",
    "app_share": "2015-07-07 12:36:57",
    "points_to_assign": "0",
    "is_followed": 0,
    "follows": {
      "users": 0,
      "brands": 0,
      "products": 0
    },
    "comments": "1",
    "wishlists": 0,
    "points": [
      {
        "brand_id": "101",
        "value": "68.00"
      }
    ]
  }
}
</pre>
<br/>

Response Example if Other
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "User data retrieved with success",
  "data": {
    "id": "4",
    "username": "lribeiro",
    "email": "lribeiro@eddmi.com",
    "phone": "919076233",
    "gender": "M",
    "birth_date": "1982-12-01",
    "token": "e873cd5fc210dd7a115a4460ed05a8d2",
    "image": null,
    "cover_image": null,
    "is_public": "1",
    "is_push_active": "1",
    "logged": "0",
    "count_followers": 0,
    "count_followos": 0
  }
}
</pre>
<br/>


<h4 id="update">Update User</h4>
HTTP Method: PUT
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/user](http://wizzyshop.eddmi.com/api/user)

Payload Example
<pre>
{
    "password": "new_password".
    "birth_date": "1982-12-01"
}
</pre>

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "User updated with success",
  "data": {
    "id": "10",
    "username": "apiguy",
    "email": "apiguy@eddmi.com",
    "phone": "919076347",
    "gender": "M",
    "birth_date": "1982-12-01",
    "token": "50f76923a454d2614eff1dc96eb3ddae",
    "image": null,
    "cover_image": null,
    "is_public": "1",
    "is_push_active": "1",
    "logged": 0
  }
}

</pre>
<br/>


<h4 id="comments">Get User Comments</h4>
HTTP Method: GET
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/user/wishlists/$user_id](http://wizzyshop.eddmi.com/api/user/wishlists/$user_id)
<br/>
$user_id: The user's to retrieve id

Response Example
<pre>
  "code": 200,
  "status": "OK",
  "message": "User's comments retrieved with success",
  "data": {
    "id": "10",
    "username": "Api Guy",
    "comments": [
      {
        "id": "9",
        "product_id": "30",
        "comment": "Greate",
        "created_at": "2015-10-06 16:44:22"
      }
    ]
  }
}
</pre>
<br/>

<h4 id="wishlists">Get User Wishlists</h4>
HTTP Method: GET
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/user/wishlists/$user_id](http://wizzyshop.eddmi.com/api/user/wishlists/$user_id)
<br/>
$user_id: The user's to retrieve id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "User's wishlists retrieved with success",
  "data": {
    "id": "10",
    "username": "Api Guy",
    "wishlists": [
      {
        "id": "11",
        "name": "Test Wishlist",
        "is_public": "1"
      }
    ]
  }
}
</pre>
<br/>


<h4 id="points">Get User Points</h4>
HTTP Method: GET
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/user/points](http://wizzyshop.eddmi.com/api/user/points)

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "User's points retrieved with success",
  "data": {
    "id": "10",
    "username": "apiguy",
    "points": []
  }
}
</pre>
<br/>


<h4 id="follows">Get User Follows</h4>
HTTP Method: GET
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/user/follows](http://wizzyshop.eddmi.com/api/user/follows/$user_id)
<br/>
$user_id: The user's to retrieve id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "User's followers retrieved with success",
  "data": {
    "id": "12",
    "username": "mk night",
    "followers": [
      {
        "id": "10",
        "username": "apiguy"
      }
      ... ...
    ]
  }
}
</pre>
<br/>


<h4 id="follow">Follow User</h4>
HTTP Method: POST
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/user/follow](http://wizzyshop.eddmi.com/api/user/follow)

Payload Example
<pre>
{
    "user_id": "10",
    "user_followed_id": "1"
}
</pre>

Response Example
<pre>
{
    "user_id": "10",
    "user_followed_id": "1"
}
</pre>
<br

<h4 id="unfollow">Unfollow User</h4>
HTTP Method: POST
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/user/unfollow](http://wizzyshop.eddmi.com/api/user/unfollow)

Payload Example
<pre>
{
    "user_id": "10",
    "user_followed_id": "1"
}
</pre>

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Unfollow with success",
  "data": null
}
</pre>
<br/>

<h4 id="images">Set/Update User Images</h4>
HTTP Method: POST
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/user/images](http://wizzyshop.eddmi.com/api/user/images)

Payload Example
<pre>
{
    "image": "image_in_form_data",
    "cover_image": "image_in_form_data"
}
</pre>

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "User's images updated with success",
  "data": {
    "image": "Image was not sent",
    "cover_image": "Cover Image was not sent"
  }
}
</pre>
<br/>
