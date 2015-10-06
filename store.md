---
layout: page
title: Stores
permalink: /stores/
---

<h3>Methods</h3>
* [Get Stores](#get-stores)
* [Get Store](#get-store)

<br/>

<h4 id="get-stores">Get Stores</h4>
HTTP Method: GET
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/store

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Stores retrived with success",
  "data": [
    {
      "id": "6",
      "name": "Adidas",
      "address": "Rua oliveira",
      "postal_code": "4740",
      "city": "Porto",
      "brand": {
        "id": "7",
        "name": "Adidas"
      }
      ... ...
    }
  ]
}
</pre>
<br/>

<h4 id="get-store">Get Store</h4>
HTTP Method: GET
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/store/:store_id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Store retrived with success",
  "data": {
    "id": "6",
    "name": "Adidas",
    "address": "Rua oliveira",
    "postal_code": "4740",
    "city": "Porto",
    "brand": {
      "id": "7",
      "name": "Adidas"
    }
  }
}
</pre>