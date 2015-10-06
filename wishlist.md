---
layout: page
title: Wishlists
permalink: /wishlists/
---

<h3>Methods</h3>
* [Get Wishlists](#get-wishlists)
* [Get Wishlist](#get-wishlist)

<br/>

<h4 id="get-wishlists">Get Wishlists</h4>
HTTP Method: GET
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/wishlist

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Wishlists retrieved with success",
  "data": {
    "user": {
      "id": "6",
      "username": "luis"
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

<h4 id="get-wishlist">Get Wishlist</h4>
HTTP Method: GET
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/wishlist/:wishlist_id

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
      "username": "luis"
    },
    "products": []
  }
}
</pre>
<br/>