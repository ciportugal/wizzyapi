---
layout: page
title: Push Notifications
permalink: /pushnotifications/
---

<h3>Methods</h3>
* [Get Push Notifications](#get)
<br/>
<br/>
<br/>

<h4 id="get">Get Push Notifications</h4>
HTTP Method: GET
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/pushnotification](http://wizzyshop.eddmi.com/api/pushnotification)
<br/>

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "User's notifications retrieved with success",
  "data": {
    "user": {
      "id": "6",
      "username": "luis"
    },
    "notifications": [
      {
        "brand": {
          "id": "1",
          "name": "Wizzyshop",
          "image": null
        },
        "id": "33",
        "message": "Ok for this push",
        "created_at": "2015-05-07 11:52:01"
      },
      {
        "brand": {
          "id": "1",
          "name": "Wizzyshop",
          "image": null
        },
        "id": "24",
        "message": "Push one more test",
        "created_at": "2015-03-16 11:00:33"
      }
      ... ...
    ]
  }
}
</pre>
<br/>


<h4 id=""></h4>
Endpoint: []()

Response Example
<pre>

</pre>

<h4 id=""></h4>
Endpoint: []()

Response Example
<pre>

</pre>

<h4 id=""></h4>
Endpoint: []()

Response Example
<pre>

</pre>

<h4 id=""></h4>
Endpoint: []()

Response Example
<pre>

</pre>