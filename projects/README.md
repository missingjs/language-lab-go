# Project-Based Learning Path

The best way to learn Go deeply is to build small but complete projects. Each project should focus on one to three core skills.

The recommended progression is:

```text
CLI → File processing → HTTP → Concurrency → Database → Background jobs → Caching → Streaming → Observability → Performance
```

For the conceptual map behind these projects, see [../roadmap.md](../roadmap.md).

---

## The Twelve Projects

1. [CLI TODO Tool](01-cli-todo/README.md) — Modules, structs, slices/maps, JSON persistence, table-driven tests.
2. [Log Analyzer](02-log-analyzer/README.md) — `bufio.Scanner`, streaming, map aggregation, benchmarks.
3. [Config Loader](03-config-loader/README.md) — Struct tags, JSON/YAML, env overrides, package API design.
4. [HTTP Health Check Service](04-health-check-service/README.md) — `net/http`, middleware, graceful shutdown, timeouts.
5. [Concurrent URL Checker](05-url-checker/README.md) — Goroutines, channels, worker pools, context timeout.
6. [In-Memory Bookmark API](06-bookmark-api/README.md) — Route design, handler layering, `httptest`.
7. [Database-Backed Bookmark API](07-bookmark-db-api/README.md) — `database/sql`, migrations, transactions, repositories.
8. [Background Job Queue](08-job-queue/README.md) — Worker pools, retries, backoff, shutdown coordination.
9. [HTTP Cache Proxy](09-cache-proxy/README.md) — `sync.RWMutex`, TTL, `singleflight`, race detector.
10. [Real-Time Log Tail Service](10-log-tail-service/README.md) — File watching, SSE/WebSocket, goroutine lifecycle.
11. [Observability Layer](11-observability-layer/README.md) — `log/slog`, Prometheus, pprof, request tracing.
12. [Performance Lab](12-performance-lab/README.md) — Benchmarks, CPU/memory profiles, allocation reduction.

---

## Recommended Project Order

```text
1. CLI TODO Tool
2. Log Analyzer
3. Config Loader
4. HTTP Health Check Service
5. Concurrent URL Checker
6. In-Memory Bookmark API
7. Database-Backed Bookmark API
8. Background Job Queue
9. HTTP Cache Proxy
10. Real-Time Log Tail Service
11. Observability Layer
12. Performance Optimization Lab
```

The progression is:

```text
Language fundamentals
→ File and IO processing
→ Package API design
→ HTTP services
→ Concurrency control
→ Service layering
→ Database integration
→ Worker systems
→ Caching and shared state
→ Streaming
→ Observability
→ Performance analysis
```

---

## Three-Version Method for Every Project

For each project, build it in three versions.

### Version 1: Make It Work

Focus on basic functionality. Avoid over-engineering.

### Version 2: Make It Idiomatic

Improve:

- Package boundaries
- Error handling
- Naming
- Interface design
- Context propagation
- Tests

### Version 3: Make It Production-Aware

Add:

- Graceful shutdown
- Timeouts
- Logging
- Metrics
- Benchmarks
- Race detector checks
- pprof where appropriate

---

## Common Go Mistakes

### Mistake 1: Writing Go Like Java

Avoid overusing:

- Manager
- Service
- Factory
- Abstract interfaces
- Large inheritance-style hierarchies

Go favors small interfaces and direct composition.

### Mistake 2: Starting Goroutines Everywhere

Concurrency is not free. Every goroutine needs a lifecycle and exit path.

### Mistake 3: Overusing Channels

Not all shared state should be modeled with channels. Sometimes a mutex is clearer.

### Mistake 4: Returning Errors Without Context

Avoid returning raw errors at important boundaries:

```go
return err
```

Prefer adding context:

```go
return fmt.Errorf("load config: %w", err)
```

### Mistake 5: Abstracting Too Early

Go encourages simple code. Avoid building complex abstractions before they are needed.

A useful Go proverb:

> A little copying is better than a little dependency.

---

## Key Questions to Ask During Every Project

```text
Is this package responsible for one clear thing?
Is this interface really necessary?
Does this error include enough context?
Is context passed correctly?
Does every goroutine have an exit path?
Can this channel block forever?
Is shared state concurrency-safe?
Do tests cover the core logic?
Does go test -race pass?
Can pprof help diagnose performance problems?
```

---

## Projects to Avoid Too Early

These can be valuable later, but they are usually too broad for early learning:

```text
A complete microservices framework
A Kubernetes operator
A high-performance RPC framework
A distributed database
A complex instant messaging system
A large e-commerce backend
A web framework from scratch
```

They combine too many concerns at once:

```text
Architecture
Deployment
Networking
Database design
Authentication
Concurrency
Performance
Observability
Business complexity
```

Early projects should focus on one to three core skills at a time.

---

## Advanced Go Practitioner Checklist

You are moving toward advanced Go proficiency when you can:

```text
Design clear package boundaries
Create simple and useful interfaces
Choose correctly between channels and mutexes
Avoid goroutine leaks
Use context for cancellation and timeouts
Write table-driven tests and benchmarks
Use the race detector and pprof effectively
Understand slice, map, and pointer memory behavior
Build production-grade HTTP services
Wrap errors with meaningful context
Avoid premature abstraction
Operate services with logging, metrics, and profiling
```
