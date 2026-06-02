[← Back to projects](../README.md)

# Project 4: HTTP Health Check Service

## Goal

Build a minimal HTTP service.

Endpoints:

```text
GET /health
GET /ready
GET /version
```

## Focus Areas

- `net/http`
- `http.Handler`
- Middleware
- Request logging
- Graceful shutdown
- Server timeouts
- Context
- Signal handling

## Completion Criteria

- Support graceful shutdown.
- Add request logging middleware.
- Configure server timeouts.
- Make the port configurable.
