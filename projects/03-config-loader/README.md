[← Back to projects](../README.md)

# Project 3: Config Loader

## Goal

Build a small configuration loader.

Support:

- JSON config
- YAML config
- Environment variable overrides
- Default values
- Validation

Example config:

```json
{
  "server_port": 8080,
  "database_url": "postgres://localhost/app",
  "log_level": "info"
}
```

Example API:

```go
cfg, err := config.Load("config.json")
if err != nil {
    return err
}
```

## Focus Areas

- Struct tags
- JSON and YAML parsing
- Environment variables
- Pointer vs value semantics
- Zero values
- Custom errors
- Package API design

## Completion Criteria

- Support default values.
- Support environment variable overrides.
- Produce clear validation errors.
- Provide tests.
- Keep the package API simple.
