[← Back to projects](../README.md)

# Project 8: Background Job Queue

## Goal

Build a small background job system.

Features:

```text
enqueue job
worker executes job
retry on failure
maximum retry count
job timeout
graceful shutdown
```

Example job types:

```text
send_email
generate_report
fetch_url
```

## Focus Areas

- Worker pools
- Channels
- Context cancellation
- Retry logic
- Backoff
- Timeout handling
- `sync.WaitGroup`
- Shutdown coordination

## Recommended Versions

- Version 1: in-memory queue
- Version 2: database-persistent queue

## Completion Criteria

- Multiple workers can run concurrently.
- Failed jobs can be retried.
- Maximum retry count is enforced.
- Graceful shutdown does not lose currently running jobs.
