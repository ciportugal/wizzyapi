---
layout: page
title: Wishlists
permalink: /wishlists/
---
<p>Allowed operations for wishlists. Note that authentication is required for all endpoints.</p>
<br/>

<h3>Methods</h3>
[Get Wishlists](#wishlists) | 
[Get Wishlist](#wishlist) | 
[Create Wishlist](#create) | 
[Update Wishlist](#update)
<br/>
<br/>
<br/>

<h4 id="wishlists">Get Wishlists</h4>
<p>Retrieve all ishlists</p>

HTTP Method: GET
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/wishlist](http://wizzyshop.eddmi.com/api/wishlist)

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Wishlists retrieved with success",
  "data": {
    "user": {
      "id": "6",
      "username": "apiguy"
    },
    "wishlists": [
      {
        "id": "16",
        "name": "fav",
        "is_public": "1",
        "products": []
      }
      ... ...
    ]
  }
}
</pre>
<br/>

<h4 id="wishlist">Get Wishlist</h4>
<p>Retrieve one ishlist</p>

HTTP Method: GET
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/wishlist/$wishlist_id](http://wizzyshop.eddmi.com/api/wishlist/$wishlist_id)
<br/>
$wishlist_id: The wishlist's id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Wishlist retrieved with success",
  "data": {
    "id": "16",
    "user_id": "6",
    "name": "fav",
    "is_public": "1",
    "user": {
      "id": "6",
      "username": "apiguy"
    },
    "products": []
  }
}
</pre>
<br/>

<h4 id="create">Create Wishlist</h4>
<p>Create a new wishlist for this user</p>

HTTP Method: POST
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/wishlist](http://wizzyshop.eddmi.com/api/wishlist)

Payload Example
<pre>
{
    "user_id": "10",
    "name": "My new Wishlist"
}
</pre>

Response Example
<pre>
{
  "code": 201,
  "status": "Created",
  "message": "Wishlist created with success",
  "data": {
    "id": "20",
    "user_id": "10",
    "name": "My new Wishlist",
    "is_public": 1,
    "added_products": 0,
    "not_added_products": 0
  }
}
</pre>
<br/>

<h4 id="update">Update Wishlist</h4>
<p>Update the user wishlist with the given id</p>

HTTP Method: PUT
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/wishlist/$wishlist_id](http://wizzyshop.eddmi.com/api/wishlist/$wishlist_id)
<br/>
$wishlist_id: The wishlist's id

Payload Example
<pre>
{
    "is_public": "0",
    "name": "My new Wishlist Updated"
}
</pre>

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Wishlist updated with success",
  "data": {
    "id": "20",
    "user_id": "10",
    "name": "My new Wishlist Updated",
    "is_public": "0",
    "added_products": 0,
    "not_added_products": 0
  }
}
</pre>
<br/>