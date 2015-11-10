---
layout: page
title: Transactions
permalink: /transactions/
---
<p>Allowed operations for transactions. Note that authentication is required for all endpoints.</p>
<br/>

<h3>Methods</h3>
[Create Transaction](#create)
<br/>
<br/>
<br/>

<h4 id="create">Create Transaction</h4>
<p>Create a transaction to give a bonus based on a gamification.</p>

HTTP Method: POST
<br/>
Requires Authentication: √
<br/>
Endpoint: [http://wizzyshop.eddmi.com/api/transaction](http://wizzyshop.eddmi.com/api/transaction)
<br/>

Example for Gamifications with ids:

* 1 - Check In at Store
* 2 - Purchase
* 3 - Share product on Facebook
* 4 - Share wishlist on Facebook
* 5 - Scan product

Payload
<pre>
{
    "brand_id": "7",
    "gamification_id": "1",
    "store_id": "6"
}
</pre>
<br/>

Response
<pre>
{
  "code": 201,
  "status": "Created",
  "message": "Transaction succefully created",
  "data": {
    "user": {
      "id": "10",
      "username": "apiguy"
    },
    "brand": {
      "id": "7",
      "name": "Ardidas"
    },
    "store": {
      "id": "6",
      "name": "Ardidas"
    },
    "balance": "1"
  }
}
</pre>
<br/>

Example for Gamifications with ids:

* 6 - Share app on Facebook
* 7 - Invite friends

Payload
<pre>
{
    "brand_id": "1", // <b style="color:red">Must be 1 (Wizzyshop)</b>
    "gamification_id": "6",
}
</pre>
<br/>

Response
<pre>
{
  "code": 201,
  "status": "Created",
  "message": "Transaction succefully created",
  "data": {
    "user": {
      "id": "10",
      "username": "apiguy"
    },
    "brand": {
      "id": "1",
      "name": "Wizzyshop"
    },
    "balance": "1"
  }
}
</pre>