---
title: "Dates and Times"
date: 2020-02-21T14:15:43+01:00
severity: should
category: properties
example_apis: []
---

When working with dates, our APIs use consistent naming and formats.

Field names should be `[something]_at`. Examples include:

* `created_at`
* `started_at`
* `last_event_at`

The format will be [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) standard, for example: `2020-02-21T14:43:23+00:00`.

### Examples

```json
{
  "created_at": "2020-02-21T14:43:23+00:00"
}
```

### Why did we choose this?

Sugested and discussed in the #api-standards channel before adoption for future APIs.

### Related Links

* [Wikipedia ISO 8601 page](https://en.wikipedia.org/wiki/ISO_8601) for more information about the format and examples
* Also used by [GitHub's API](https://developer.github.com/v3/#schema)
