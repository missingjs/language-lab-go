[← Back to projects](../README.md)

# Project 9: HTTP Cache Proxy

## Goal

Build a small API proxy with caching.

Example endpoint:

```text
GET /fetch?url=https://example.com
```

Behavior:

```text
Check cache
Return cached response on hit
Fetch remote response on miss
Save response with TTL
```

## Focus Areas

- In-memory cache
- `sync.Mutex` and `sync.RWMutex`
- TTL
- Eviction
- `singleflight`
- HTTP client timeouts
- Race detector

## Completion Criteria

- Cache is concurrency-safe.
- TTL is supported.
- Maximum cache size is supported.
- `go test -race` passes.
- Duplicate concurrent fetches for the same URL are avoided.

## Advanced Challenges

- Implement LRU eviction.
- Add singleflight protection.
- Add metrics.
