---
layout: page
title: Scans
permalink: /scans/
---
<p>Allowed operations for scans. Note that authentication is required for some endpoints.</p>
<br/>


<h3>Methods</h3>
[Get Scans](#scans) | 
[Get Scan](#scan) | 
[Add Scan](#add)
<br/>
<br/>
<br/>

<h4 id="scans">Get Scans</h4>
HTTP Method: GET
<br/>
Requires Authentication: x
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/scan](http://wizzyshop.eddmi.com/api/scan)

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

<h4 id="scan">Get Scan</h4>
HTTP Method: GET
<br/>
Requires Authentication: x
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/scan/$scan_id](http://wizzyshop.eddmi.com/api/scan/$scan_id)
<br/>
$scan_id: The scan's id

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
<br/>

<h4 id="add">Add Scan</h4>
HTTP Method: POST
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/scan/](http://wizzyshop.eddmi.com/api/scan/)
<br/>

Payload Example
<pre>
{
    "scan_id": "2"
}
</pre>
<br/>

Response Example
<pre>
{
  "code": 201,
  "status": "Created",
  "message": "Scan successfully created",
  "data": {
    "user": {
      "id": "3",
      "username": "apiguy",
      "balance": 0
    }
  }
}
</pre>
<br/>