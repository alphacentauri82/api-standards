---
title: "Data Structure"
date: 2018-07-31T02:53:21+01:00
severity: must
category: properties
example_apis: []
---

We aim to use consistent terminology across all APIs. Here are the commonly used property names:

* `[resource]_id` - A string that identifies a specific resource
* `to` - The identifier of a message or conversation recipient. This represents either the app sending an outbound message or the user contacting the app with an inbound messages
* `from` - The identifier of a message sender or the initiator of a conversation. This represents either the app sending an outbound message or the user contacting the app with an inbound messages
* `reference` - The reference associating this request with the customer's internal data systems.
* `[description]_url` - A url that is necessary for communication. For example, `callback_url`.
* `[description]_method` - Send the callback using either GET or POST.
* `ttl` - Total time to live is the time during which this request is valid.
* `mccmnc` - the country and carrier code for the carrier who handled your request.
* `language` - The language used for the communication in https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes. For example, en-US
* `count` - The number of parts your message was divided into in order to be sent correctly.
* `total` - The amount of objects found as a result of a search request.
* `direction` - Inbound (MO) or Outbound (MT)
* `started_at` - The time the communication started in https://en.wikipedia.org/wiki/ISO_8601 format.
* `ended_at` - The time the communication ended in https://en.wikipedia.org/wiki/ISO_8601 format.
* `duration` - The duration of the call in seconds.
* `balance` - The amount of money left in your Nexmo account.
* `rate` - The price for each request. This is per request for text based messages, or per second for voice.
* `cost` - The total cost that is the result of the request. 

### Examples

For some properties the data should be represented in a specific format.

* Each API defines a single data structure and set of properties (resource). This must be coherent with the other APIs.
* The data structure must be uniform regardless of the context. An SMS record is always the same, a number is always the same.
* Data structures can be used as properties of other responses.

#### Endpoint

```json
{
  "endpoint": {
    "type": "phone",
    "number": "14155550100"
  }
}
```

### Why did we choose this?

Pre-existing standard

### Related Links

N/A
