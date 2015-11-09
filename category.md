---
layout: page
title: Categories
permalink: /categories/
---

<h3>Methods</h3>
* [Get Categories](#categories)
* [Get Category](#category)
<br/>
<br/>
<br/>

<h4 id="categories">Get Categories</h4>
HTTP Method: GET
<br/>
Requires Authentication: x
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/category](http://wizzyshop.eddmi.com/api/category)

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Categories retrieved with success",
  "data": [
    {
      "id": "1",
      "name": "Men",
      "description": "Men",
      "count_products": "10"
    },
    {
      "id": "2",
      "name": "Women",
      "description": "Women",
      "count_products": "3"
    },
    {
      "id": "3",
      "name": "Accessories",
      "description": "Accessories",
      "count_products": 0
    },
    ... ...
  ]
}
</pre>
<br/>

<h4 id="category">Get Category</h4>
HTTP Method: GET
<br/>
Requires Authentication: x
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/category/$category_id](http://wizzyshop.eddmi.com/api/category/$category_id)
<br/>
$category_id: The category's id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Category retrieved with success",
  "data": {
    "id": "1",
    "name": "Men",
    "description": "Men",
    "count_products": "10"
  }
}
</pre>
