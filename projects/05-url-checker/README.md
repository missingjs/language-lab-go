[← Back to projects](../README.md)

# Project 5: Concurrent URL Checker

## Goal

Build a tool that checks whether a list of URLs is reachable.

Example command:

```text
urlcheck urls.txt --concurrency 20 --timeout 2s
```

Example output:

```text
OK      https://example.com       200   120ms
FAILED  https://bad.example.com   timeout
```

## Focus Areas

- Goroutines
- Channels
- Worker pools
- Context timeout
- `http.Client`
- Concurrency limits
- Graceful cancellation
- Result aggregation

## Key Questions

- How do you limit maximum concurrency?
- How do you handle timeouts?
- How do you avoid goroutine leaks?
- How do you handle Ctrl+C cleanly?

## Completion Criteria

- Configurable concurrency.
- Request timeout support.
- Cancellation support.
- No goroutine leaks.
- Tests for core behavior.
