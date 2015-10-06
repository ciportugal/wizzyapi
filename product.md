---
layout: page
title: Products
permalink: /products/
---

<h3>Methods</h3>
* [Get Products](#get-products)
* [Get Product](#get-product)
* [Get Product Followers](#get-product-followers)
* [Add Product Follower](#post-product-follower)

<br/>

<h4 id="get-products">Get Products</h4>
HTTP Method: GET
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/product

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Products retrieved with success",
  "data": {
    "products": [
      {
        "id": "30",
        "name": "Footbal Boot",
        "description": "Adidas Footbal Boot",
        "price": "120.00",
        "old_price": null,
        "count_comments": "1",
        "count_followers": 0,
        "count_promotions": 0,
        "count_wishlists": "1",
        "photos": [
          "product/30/1.png",
          "product/30/2.png"
        ],
        "scans": [
          {
            "id": "2",
            "product_id": "30",
            "barcode": "0000000000000000000"
          }
        ],
        "brand": {
          "id": "7",
          "name": "Adidas",
          "image": "brand/7/image.png"
        }
      },
      ... ... 
    ],
    "paging": {
      "page": 1,
      "count": 16,
      "next_page": false,
      "page_count": 1
    }
  }
}
</pre>
<br/>

<h4 id="get-product">Get Product</h4>
HTTP Method: GET
<br/>
Endpoin
Endpoint: http://wizzyshop.eddmi.com/index.php/api/product/:product_id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Product retrieved with success",
  "data": {
    "id": "30",
    "name": "Footbal Boot",
    "description": "Adidas Footbal Boot",
    "price": "120.00",
    "old_price": null,
    "count_comments": "1",
    "count_followers": 0,
    "count_promotions": 0,
    "count_wishlists": "1",
    "photos": [
      "product/30/1.png",
      "product/30/2.png"
    ],
    "categories": [
      {
        "id": "1",
        "name": "Men",
        "description": "Men"
      }
    ],
    "scans": [
      {
        "id": "2",
        "product_id": "30",
        "barcode": "0000000000000000000"
      }
    ],
    "brand": {
      "id": "7",
      "name": "Adidas",
      "image": "brand/7/image.png"
    }
  }
}
</pre>
<br/>

<h4 id="get-product-followers">Get Product Followers</h4>
HTTP Method: GET
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/product/followers/:product_id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Product's followers retrieved with success",
  "data": {
    "id": "30",
    "name": "Footbal Boot",
    "description": "Adidas Footbal Boot",
    "price": "120.00",
    "followers": [
      {
        "id": "1",
        "username": "Salvador Martinha"
      },
      ... ...
    ]
  }
}
</pre>
<br/>

<h4 id="post-product-follower">Add Product Follower</h4>
HTTP Method: POST
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/product/follow


Payload Example
<pre>
{
  "product_id": 30,
  "user_id": 1
}
</pre>

Response Example
<pre>
{
  "code": 201,
  "status": "Created",
  "message": "User is now following this product",
  "data": {
    "user_id": 1,
    "product_id": 30
  }
}
</pre>
<br/>

<h4 id=""></h4>
Endpoint: []()

Response Example
<pre>

</pre>