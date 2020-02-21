---
title: "HTTP Verbs"
date: 2018-07-31T01:16:58+01:00
severity: must
category: request
example_apis: []
---

- Use HTTP methods to map CRUD actions on Resources i.e. 
  - POST creates a new Resources in a Collection (see also [201 status](/api-standards/http-code/201) )
  - DELETE removes a Resource
  - GET lists Resources
  - PUT replaces a complete Resource
  - PATCH partially updates a Resource

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

* [RFC2616](https://tools.ietf.org/html/rfc2616#section-9)
