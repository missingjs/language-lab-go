[← Back to projects](../README.md)

# Project 2: Log Analyzer

## Goal

Build a tool that reads log files and outputs statistics.

Example input:

```text
2026-01-01T10:00:00Z GET /api/users 200 23ms
2026-01-01T10:00:01Z POST /api/login 500 80ms
```

Example output:

```text
Total requests: 12000
Status 200: 10300
Status 500: 87
Top paths:
/api/users 3200
/api/login 900
Slowest endpoints:
...
```

## Focus Areas

- `os.Open`
- `bufio.Scanner`
- `io.Reader`
- String parsing
- Map aggregation
- Error wrapping
- Streaming processing
- Benchmarks

## Advanced Challenges

- Support 1GB log files.
- Do not load the entire file into memory.
- Output both JSON and CSV.
