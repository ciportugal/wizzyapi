---
layout: page
title: Products
permalink: /products/
---

<h3>Methods</h3>
* [Get Products](#products)
* [Get Product](#product)
* [Get Product Followers](#followers)
* [Add Product Follower](#add-follower)
* [Delete Product Follower](#delete-follower)
* [Get Product Comments](#comments)
* [Add Product Comment](#add-comment)
* [Get Product Wishlists](#wishlists)
* [Get Product Promotions](#promotions)
* [Get Product Scans](#scans)
<br/>
<br/>
<br/>

<h4 id="products">Get Products</h4>
HTTP Method: GET
<br/>
Requires Authentication: x
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/product](http://wizzyshop.eddmi.com/api/product)

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

<h4 id="product">Get Product</h4>
HTTP Method: GET
<br/>
Requires Authentication: x
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/product/$product_id](http://wizzyshop.eddmi.com/api/product/$product_id)
<br/>
$product_id: The product's id

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

<h4 id="followers">Get Product Followers</h4>
HTTP Method: GET
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/product/followers/$product_id](http://wizzyshop.eddmi.com/api/product/followers/$product_id)
<br/>
$product_id: The product's id

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

<h4 id="add-follower">Add Product Follower</h4>
HTTP Method: POST
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/product/follow](http://wizzyshop.eddmi.com/api/product/follow)


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

<h4 id="delete-follower">Delete Product Follower</h4>
HTTP Method: POST
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/product/unfollow](http://wizzyshop.eddmi.com/api/product/unfollow)

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
  "code": 200,
  "status": "OK",
  "message": "Unfollow with success",
  "data": null
}
</pre>
<br/>

<h4 id="comments">Get Product Comments</h4>
HTTP Method: GET
<br/>
Requires Authentication: x
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/product/comments/$product_id](http://wizzyshop.eddmi.com/api/product/comments/$product_id)
<br/>
$product_id: The product's id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Product's comments retrieved with success",
  "data": {
    "id": "30",
    "name": "Footbal Boot",
    "description": "Adidas Footbal Boot",
    "price": "120.00",
    "comments": [
      {
        "id": "7",
        "comment": "amazing boots",
        "updated_at": "2015-06-16 00:58:22",
        "user": {
          "id": "5",
          "username": "miguel",
          "image": "user/5/image.png"
        },
        ... ...
      }
    ]
  }
}
</pre>
<br/>

<h4 id="add-comment">Add Product Comment</h4>
HTTP Method: POST
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/product/comment](http://wizzyshop.eddmi.com/api/product/comment)

Payload Example
<pre>
{
  "user_id": 1,
  "product_id": 30,
  "comment": "OK"
}
</pre>

Response Example
<pre>
{
  "code": 201,
  "status": "Created",
  "message": "Comment created with success",
  "data": {
    "id": "9"
  }
}
</pre>
<br/>

<h4 id="wishlists">Get Product Wishlists</h4>
HTTP Method: GET
<br/>
Requires Authentication: √
<br/>
Endpoint:[http://wizzyshop.eddmi.com/api/product/wishlists/$product_id](http://wizzyshop.eddmi.com/api/product/wishlists/$product_id)
<br/>
$product_id: The product's id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Product's wishlists retrieved with success",
  "data": {
    "id": "30",
    "name": "Footbal Boot",
    "description": "Adidas Footbal Boot",
    "price": "120.00",
    "wishlists": [
      {
        "id": "18",
        "user_id": "5",
        "name": "shoes",
        "is_public": "1"
      }
    ]
  }
}
</pre>
<br/>

<h4 id="promotions">Get Product Promotions</h4>
HTTP Method: GET
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/product/promotions/$product_id](http://wizzyshop.eddmi.com/api/product/promotions/$product_id)
<br/>
$product_id: The product's id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Product's wishlists retrieved with success",
  "data": {
    "id": "30",
    "name": "Footbal Boot",
    "description": "Adidas Footbal Boot",
    "price": "120.00",
    "promotions": []
  }
}
</pre>
<br/>

<h4 id="scans">Get Product Scans</h4>
HTTP Method: GET
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/product/scans/$product_id](http://wizzyshop.eddmi.com/api/product/scans/$product_id)
<br/>
$product_id: The product's id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Product's scans retrieved with success",
  "data": {
    "id": "30",
    "name": "Footbal Boot",
    "description": "Adidas Footbal Boot",
    "price": "120.00",
    "scans": [
      {
        "id": "2"
      }
    ]
  }
}
</pre>
<br/>