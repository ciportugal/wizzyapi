---
layout: page
title: Stores
permalink: /stores/
---
<p>Allowed operations for brands. Note that authentication is required for some endpoints.</p>
<br/>

<h3>Methods</h3>
[Get Stores](#stores) | 
[Get Store](#store)
<br/>
<br/>
<br/>

<h4 id="stores">Get Stores</h4>
<p>Retrieve all stores</p>

HTTP Method: GET
<br/>
Requires Authentication: x
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/store](http://wizzyshop.eddmi.com/api/store)

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Stores retrived with success",
  "data": [
    {
      "id": "6",
      "name": "Ardidas",
      "address": "Rua oliveira",
      "postal_code": "4740",
      "city": "Porto",
      "brand": {
        "id": "7",
        "name": "Ardidas"
      }
      ... ...
    }
  ]
}
</pre>
<br/>

<h4 id="store">Get Store</h4>
<p>Retrieve one store</p>

HTTP Method: GET
<br/>
Requires Authentication: x
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/store/$store_id](http://wizzyshop.eddmi.com/api/store/$store_id)
<br/>
$store_id: The store's id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Store retrived with success",
  "data": {
    "id": "6",
    "name": "Ardidas",
    "address": "Rua oliveira",
    "postal_code": "4740",
    "city": "Porto",
    "brand": {
      "id": "7",
      "name": "Ardidas"
    }
  }
}
</pre>