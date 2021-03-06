---
title: "PuppetDB 1.6 » API » v3 » Querying Server Time"
layout: default
canonical: "/puppetdb/latest/api/query/v3/server-time.html"
---

[curl]: ../curl.html#using-curl-from-localhost-non-sslhttp

The `/server-time` endpoint can be used to retrieve the server time from the PuppetDB server.

## Routes

### `GET /v3/server-time`

This query endpoint will return the current time of the clock on the PuppetDB
server.  This can be useful as input to other time-based queries against PuppetDB,
to eliminate the possibility of time differences between the clocks on client
machines.

#### Examples

[Using `curl` from localhost][curl]:

    curl -X GET http://localhost:8080/v3/server-time

    {"server-time": "2013-09-20T20:54:27.472Z"}

## Response Format

The response will be in `application/json`, and will return a JSON map with a
single key: `server-time`, whose value is an ISO-8601 representation of the
current time on the PuppetDB server.

    {"server-time": "2013-09-20T20:54:27.472Z"}
