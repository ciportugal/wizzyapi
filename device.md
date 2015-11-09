---
layout: page
title: Devices
permalink: /devices/
---
<p>Allowed operations for devices. Note that authentication is required for all endpoints.</p>
<br/>

<h3>Methods</h3>
[Add Device](#device)
<br/>
<br/>
<br/>

<h4 id="device">Add Device</h4>
HTTP Method: POST
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/device](http://wizzyshop.eddmi.com/api/device)
<br/>

Payload Example
<pre>
{
    "user_id":"1",
    "push_token": "wwdsadwqe234feswrw",
    "device_identifier": "3424erwe4325",
    "client_type": "iOS"
}
</pre>
<br/>

Response Example
<pre>
{
  "code": 201,
  "status": "Created",
  "message": "Device successfully added",
  "data": null
}
</pre>

