[← Back to projects](../README.md)

# Project 1: CLI TODO Tool

## Goal

Build a command-line TODO application.

Example commands:

```text
todo add "learn Go"
todo list
todo done 1
todo remove 1
```

## Focus Areas

- Go modules
- Basic package organization
- Structs
- Slices and maps
- JSON file persistence
- Error handling
- Table-driven tests
- CLI argument parsing

## Suggested Structure

```text
todo/
├── cmd/
│   └── todo/
│       └── main.go
├── internal/
│   └── task/
├── go.mod
└── tasks.json
```

## Completion Criteria

- Add, list, complete, and remove tasks from the command line.
- Persist data to a local file.
- Write tests for core task logic.
- Return clear error messages.
