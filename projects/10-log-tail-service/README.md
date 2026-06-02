[← Back to projects](../README.md)

# Project 10: Real-Time Log Tail Service

## Goal

Build a simplified `tail -f` service over HTTP.

Endpoints:

```text
GET /logs
GET /logs/stream
```

The streaming endpoint can use Server-Sent Events or WebSocket.

## Focus Areas

- File watching
- Streaming responses
- SSE or WebSocket
- Context cancellation
- Client disconnect handling
- Goroutine lifecycle
- Backpressure

## Key Questions

- Does a goroutine exit when a client disconnects?
- How do you read only newly appended log data?
- Can slow clients overload the server?
