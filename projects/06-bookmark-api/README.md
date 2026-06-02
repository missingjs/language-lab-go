[← Back to projects](../README.md)

# Project 6: In-Memory Bookmark API

## Goal

Build a REST API without relying on a large framework.

Example endpoints:

```text
POST   /bookmarks
GET    /bookmarks
GET    /bookmarks/{id}
DELETE /bookmarks/{id}
```

Start with an in-memory map.

## Focus Areas

- Route design
- Handler layering
- JSON request and response handling
- Consistent error responses
- Middleware
- Interface design
- Testing with `httptest`

## Suggested Structure

```text
bookmarkd/
├── cmd/
│   └── server/
├── internal/
│   ├── httpapi/
│   ├── bookmark/
│   └── store/
└── go.mod
```

Possible store interface:

```go
type Store interface {
    Create(ctx context.Context, b Bookmark) error
    List(ctx context.Context) ([]Bookmark, error)
    Delete(ctx context.Context, id string) error
}
```

## Completion Criteria

- HTTP handlers do not directly manipulate the map.
- Business logic and HTTP logic are separated.
- Error responses are consistent.
- Handlers are tested.
