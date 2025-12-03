# Apple School Manager: OpenAPI 2.0 spec (Swagger)

## What's in this directory?

### Source files: /src/*

A split version of the OpenAPI 2.0 spec, where changes should be made.

### Compiled spec: openapi.yaml

The compiled version of the OpenAPI spec, for consumption by different tools.

It is compiled with [redocly](https://github.com/Redocly/redocly-cli).

## How to make changes?

1. Update the `/src` files
2. Compile the full spec from the source files, pointing to the entrypoint/top-level file:
```bash
npx @redocly/cli@latest bundle src/openapi.yaml -o openapi.yaml
```
3. Lint the compiled spec for any errors or warnings that need to be addressed:
```bash
npx @redocly/cli@latest lint openapi.yaml
```