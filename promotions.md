---
layout: page
title: Promotions
permalink: /promotions/
---

<h3>Methods</h3>
* [Get Promotions](#promotions)
* [Get Promotion](#promotion)
* [Get Promotion's Products](#products)
<br/>
<br/>
<br/>

<h4 id="promotions">Get Promotions</h4>
HTTP Method: GET
<br/>
Requires Authentication: x
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/promotion](http://wizzyshop.eddmi.com/api/promotion)

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Promotions retrieved with success",
  "data": [
    {
      "id": "2",
      "name": "Up to 50%",
      "description": "Up to 50%",
      "image": "promotion/2/image.png",
      "expiration_date": "2015-12-31 00:00:00",
      "count_products": "1",
      "brand": {
        "id": "7",
        "name": "Adidas"
      },
      ... ...
    }
  ]
}
</pre>
<br/>

<h4 id="promotion">Get Promotion</h4>
HTTP Method: GET
<br/>
Requires Authentication: x
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/promotion/$promotion_id](http://wizzyshop.eddmi.com/api/promotion/$promotion_id)
<br/>
$promotion_id: The promotion's id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Promotion retrieved with success",
  "data": {
    "id": "2",
    "name": "Up to 50%",
    "description": "Up to 50%",
    "image": "promotion/2/image.png",
    "expiration_date": "2015-12-31 00:00:00",
    "brand": {
      "id": "7",
      "name": "Adidas"
    },
    "products": [
      {
        "id": "15",
        "name": "Sandals",
        "description": "Adidas Sandals",
        "price": "45.00",
        "photos": [
          "product/15/1.png",
          "product/15/2.png",
          "product/15/3.png"
        ]
      },
      ... ...
    ]
  }
}
</pre>
<br/>

<h4 id="products">Get Promotion's Products</h4>
HTTP Method: GET
<br/>
Requires Authentication: x
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/promotion/products/$promotion_id](http://wizzyshop.eddmi.com/api/promotion/products/$promotion_id)
<br/>
$promotion_id: The promotion's id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Promotion retrieved with success",
  "data": {
    "id": "2",
    "name": "Up to 50%",
    "description": "Up to 50%",
    "image": "promotion/2/image.png",
    "expiration_date": "2015-12-31 00:00:00",
    "brand": {
      "id": "7",
      "name": "Adidas"
    },
    "products": [
      {
        "id": "15",
        "name": "Sandals",
        "description": "Adidas Sandals",
        "price": "45.00",
        "photos": [
          "product/15/1.png",
          "product/15/2.png",
          "product/15/3.png"
        ]
      },
      ... ...
    ]
  }
}
</pre>
