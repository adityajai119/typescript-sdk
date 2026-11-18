---
'@modelcontextprotocol/hono': patch
---

`createMcpHonoApp` now skips JSON body parsing for `GET` and `HEAD` requests and leaves `parsedBody` unset when an `application/json` request has an empty body, instead of answering `400 Invalid JSON` before downstream routes and MCP handlers run.
