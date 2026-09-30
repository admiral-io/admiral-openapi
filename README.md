# admiral-openapi

OpenAPI specifications for the [Admiral](https://admiral.io/?utm_source=github&utm_medium=referral&utm_campaign=admiral-openapi) API. Use these specs to generate HTTP clients, explore endpoints, or integrate with API tooling.

## Documentation

[View Interactive API Docs](https://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/admiral-io/admiral-openapi/master/openapi.v3.yaml)

## Files

| File | Version |
|------|---------|
| `openapi.v3.yaml` | OpenAPI 3.1 |
| `openapi.swagger.yaml` | OpenAPI 2.0 (Swagger) |

## Usage

### Raw URLs

```
https://raw.githubusercontent.com/admiral-io/admiral-openapi/master/openapi.v3.yaml
https://raw.githubusercontent.com/admiral-io/admiral-openapi/master/openapi.swagger.yaml
```

### Client Generation

**Go (oapi-codegen)** - uses OpenAPI 2.0:

```bash
go install github.com/oapi-codegen/oapi-codegen/v2/cmd/oapi-codegen@latest
oapi-codegen -package api openapi.swagger.yaml > api/client.go
```

**Go (openapi-generator)** - uses OpenAPI 3.1:

```bash
openapi-generator-cli generate -i openapi.v3.yaml -g go -o ./client/go
```

**TypeScript**:

```bash
openapi-generator-cli generate -i openapi.v3.yaml -g typescript-fetch -o ./client/ts
```

**Python**:

```bash
openapi-generator-cli generate -i openapi.v3.yaml -g python -o ./client/python
```

## Admiral

[Admiral](https://admiral.io/?utm_source=github&utm_medium=referral&utm_campaign=admiral-openapi) is a control plane for coordinating infrastructure and application delivery across environments. This repository is one of its
[open-source tools](https://github.com/admiral-io).

- [Documentation](https://admiral.io/docs?utm_source=github&utm_medium=referral&utm_campaign=admiral-openapi)
- A bug in this repository: [open an issue](https://github.com/admiral-io/admiral-openapi/issues/new/choose)
- Anything else about Admiral, or not sure where it goes: [admiral-community](https://github.com/admiral-io/admiral-community)
- A security vulnerability: email [security@admiral.io](mailto:security@admiral.io), never a public issue
