---
layout: page
title: Scans
permalink: /scans/
---

<h3>Methods</h3>
* [Get Scans](#get-scans)
* [Get Scan](#get-scan)

<br/>

<h4 id="get-scans">Get Scans</h4>
HTTP Method: GET
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/scan

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Scans retrieved with success",
  "data": [
    {
      "id": "2",
      "barcode": "0000000000000000000",
      "brand": {
        "id": "7",
        "name": "Adidas"
      },
      "product": {
        "id": "30",
        "name": "Footbal Boot",
        "description": "Adidas Footbal Boot",
        "price": "120.00",
        "old_price": null,
        "images": []
      }
    }
    ... ...
  ]
}
</pre>
<br/>

<h4 id="get-scan">Get Scan</h4>
HTTP Method: GET
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/scan/2

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Scan retrieved with success",
  "data": {
    "id": "2",
    "barcode": "0000000000000000000",
    "brand": {
      "id": "7",
      "name": "Adidas"
    },
    "product": {
      "id": "30",
      "name": "Footbal Boot",
      "description": "Adidas Footbal Boot",
      "price": "120.00",
      "old_price": null,
      "images": []
    }
  }
}
</pre>