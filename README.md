# MimePost Go SDK

This repository contains a simple, beginner friendly Go SDK generated from a
Postman collection. The collection lives in `postman.json` and can be
regenerated at any time using `go generate`.

## Generating code

```bash
go generate ./sdk
```

This reads the Postman collection and creates type-safe helper methods inside
`sdk/generated.go`.

## Using the SDK

```go
client := sdk.NewClient("https://api.example.com", "API_KEY")
resp, err := client.Ping(context.Background())
```

Replace `postman.json` with your own collection to generate methods for your
endpoints.
