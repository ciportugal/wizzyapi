---
layout: page
title: Promotions
permalink: /promotions/
---

<h3>Methods</h3>
* [Get Promotions](#promotions)
* [Get Promotion](#promotion)

<br/>

<h4 id="promotions">Get Promotions</h4>
HTTP Method: GET
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/promotion

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

<h4 id="promotion">Get Promotion</h4>
HTTP Method: GET
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/promotion/:promotion_id

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
