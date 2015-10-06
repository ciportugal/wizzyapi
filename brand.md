---
layout: page
title: Brands
permalink: /brands/
---

###Methods
* [Get Brands](#brands)
* [Get Brand](#brand)
* [Get Brand Followers](#followers)
* [Get Brand Products](#products)
* [Get Brand Promotions](#promotions)
* [Get Brand Scans](#scans)
* [Add Brand Follower](#add-follower)
* [Delete Brand Follower](#delete-follower)
<br/>


<h4 id="brands">Get Brands</h4>
HTTP Method: GET
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/brand

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Brands retrived with success",
  "data": [
    {
      "id": "8",
      "name": "Church's",
      "description": "English Shoes",
      "image": "brand/8/image.png",
      "cover_image": "brand/8/cover_image.png",
      "count_followers": "2",
      "count_products": "3",
      "count_promotions": 0,
      "count_scans": 0,
      "points_conversion": [
        {
          "id": "10",
          "points": "1000.00",
          "percentage": "5.00"
        },
        {
          "id": "11",
          "points": "2000.00",
          "percentage": "10.00"
        }
      ]
    },
    ... ...
  ]
}
</pre>
<br/>

<h4 id="brand">Get Brand</h4>
HTTP Method: GET
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/brand/:brand_id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Brand retrieved with success",
  "data": {
    "id": "8",
    "name": "Church's",
    "description": "English Shoes",
    "image": "brand/8/image.png",
    "cover_image": "brand/8/cover_image.png",
    "count_followers": "2",
    "count_products": "3",
    "count_promotions": 0,
    "count_scans": 0,
    "points_conversion": [
      {
        "id": "10",
        "points": "1000.00",
        "percentage": "5.00"
      },
      {
        "id": "11",
        "points": "2000.00",
        "percentage": "10.00"
      }
    ]
  }
}
</pre>
<br/>

<h4 id="followers">Get Brand Followers</h4>
HTTP Method: GET
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/brand/followers/:brand_id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Brand's followers retrieved with success",
  "data": {
    "id": "8",
    "name": "Church's",
    "followers": [
      {
        "id": "3",
        "username": "jmteixeira"
      },
      {
        "id": "5",
        "username": "miguel"
      },
      ... ...
    ]
  }
}
</pre>
<br/>

<h4 id="products">Get Brand Products</h4>
HTTP Method: GET
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/brand/products/:brand_id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Brand's products retrieved with success",
  "data": {
    "id": "8",
    "name": "Church's",
    "products": [
      {
        "id": "17",
        "name": "Penny loafers",
        "description": "Penny loafers",
        "price": "105.00",
        "old_price": null,
        "photos": [
          "product/17/1.png",
          "product/17/2.png",
          "product/17/3.png"
        ]
      },
      {
        "id": "18",
        "name": "Classic loafers",
        "description": "Classic loafers",
        "price": "75.00",
        "old_price": null,
        "photos": [
          "product/18/1.png",
          "product/18/2.png",
          "product/18/3.png"
        ]
      },
      ... ...
    ]
  }
}
</pre>
<br/>

<h4 id="promotions">Get Brand Promotions</h4>
HTTP Method: GET
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/brand/promotions/:brand_id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Brand's promotions retrieved with success",
  "data": {
    "id": "8",
    "name": "Church's",
    "promotions": []
  }
}
</pre>
<br/>

<h4 id="scans">Get Brand Scans</h4>
HTTP Method: GET
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/brand/scans/:brand_id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Brand's scans retrieved with success",
  "data": {
    "id": "8",
    "name": "Church's",
    "scans": []
  }
}
</pre>
<br/>

<h4 id="add-follower">Add Brand Follower</h4>
HTTP Method: POST
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/brand/follow

Payload Example
<pre>
{
  "brand_id": 8,
  "user_id": 1
 }
</pre>

Response Example
<pre>
{
  "code": 201,
  "status": "Created",
  "message": "User is now following this brand",
  "data": {
    "user_id": 1,
    "brand_id": 8
  }
}
</pre>
<br/>

<h4 id="delete-follower">Delete Brand Follower</h4>
HTTP Method: POST
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/brand/unfollow

Payload Example
<pre>
{
  "brand_id": 8,
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