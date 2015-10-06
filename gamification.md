---
layout: page
title: Gamification
permalink: /gamification/
---

<h3>Methods</h3>
* [Get Gamifications](#gamifications)
* [Get Gamification](#gamification)

<br/>

<h4 id="gamifications">Get Gamifications</h4>
HTTP Method: GET
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/gamification

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Gamifications retrived with success",
  "data": [
    {
      "id": "1",
      "name": "Check In",
      "points": "1"
    },
    {
      "id": "2",
      "name": "Compra",
      "points": "1"
    },
    {
      "id": "3",
      "name": "Partilha de produto no facebook",
      "points": "1"
    },
    {
      "id": "4",
      "name": "Partilha de lista no facebook",
      "points": "1"
    },
    {
      "id": "5",
      "name": "Scan de produto",
      "points": "1"
    },
    .. ...
  ]
}
</pre>
<br/>

<h4 id="gamification">Get Gamification</h4>
HTTP Method: GET
<br/>
Endpoint: http://wizzyshop.eddmi.com/index.php/api/gamification/:gamification_id

Response Example
<pre>
{
  "code": 200,
  "status": "OK",
  "message": "Gamification retrieved with success",
  "data": {
    "id": "1",
    "name": "Check In",
    "points": "1"
  }
}
</pre>