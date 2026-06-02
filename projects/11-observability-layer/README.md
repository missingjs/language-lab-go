[← Back to projects](../README.md)

# Project 11: Observability Layer

## Goal

Add observability to one of the earlier services.

Features:

```text
/metrics
/debug/pprof
structured logging
request ID
latency histogram
error count
```

## Focus Areas

- `log/slog`
- Prometheus metrics
- OpenTelemetry basics
- pprof
- Middleware
- Request tracing
- Production diagnostics

## Completion Criteria

- Every request has a request ID.
- Request latency is measurable.
- Error counts are visible.
- pprof is available.
- Slow endpoints can be diagnosed.
