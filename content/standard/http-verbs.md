---
title: "HTTP Verbs"
date: 2018-07-31T01:16:58+01:00
severity: must
category: request
example_apis: []
---

- Use HTTP methods appropriately for the operation you are performing. CRUD (Create, Read, Update, Delete) operations and the correct response for each are as follows:
  - GET lists Resources in a Collection, or a single Resource, returning a [200 status](/api-standards/http-code-200) and the requested Resource(s)
  - POST creates a new Resource in a Collection, returning a [201 status](/api-standards/http-code/201) and the new Resource
  - PUT replaces a complete Resource with the supplied representation, returning a [200 status](/api-standards/http-code-200) and the udpated Resource
  - PATCH partially updates a Resource with the supplied fields, returning a [200 status](/api-standards/http-code-200) and the udpated Resource
  - DELETE removes a Resource, returning a [204 status](/api-standards/http-code/204) status and no body

### Examples

- `GET members/` - lists all the resources of the collection members
- `GET members/bob` - lists the details of bob who is a resources of the collection members
- `POST members -d '{"name": "Harry", "age": 22, "phone_number": "14155550100"}'` - create a new member called Harry
- `PUT members/harry -d '{"name": "Harry", "age": 23, "phone_number": "14155550100"}'` - replace all of Harry's details
- `PATCH members/harry -d '{"age": 23}'` - update Harry's age only
- `DELETE members/steve` - remove the member Steve from the collection

### Why did we choose this?

Pre-existing standard

### Related Links

* The [Method Definitions in the RFC2616 HTTP 1.1 spec](https://tools.ietf.org/html/rfc2616#section-9) are relevant to this part of API design.
* For the not-so-happy path, there are [error format guidelines](/api-standards/standard/errors) to guide you.
* All responses should follow [HAL-JSON format](/api-standards/standard/hal-json).
