[← Back to projects](../README.md)

# Project 12: Performance Optimization Lab

## Goal

Choose one previous project and optimize it with measurement.

Good candidates:

- Log analyzer
- Cache proxy
- URL checker
- Bookmark API

Goals:

- Find CPU hotspots.
- Find memory allocation hotspots.
- Reduce unnecessary allocations.
- Write benchmarks.
- Use pprof to validate improvements.

## Focus Areas

- Benchmarks
- `go test -bench`
- `go test -benchmem`
- CPU profiles
- Memory profiles
- Escape analysis
- Allocation reduction

## Completion Criteria

- Establish a benchmark baseline.
- Make an optimization.
- Compare before and after results.
- Explain why the performance changed.
- Avoid guessing.
