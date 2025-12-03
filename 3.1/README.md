# Apple School Manager: OpenAPI 3.1 spec

## What's in this directory?

### Source files: /src/*

A split version of the OpenAPI spec, where changes should be made.

This directory was created by first writing the spec as one file, and then validating and splitting it with [redocly](https://github.com/Redocly/redocly-cli):

```bash
npx @redocly/cli@latest lint openapi.yaml
npx @redocly/cli@latest split openapi.yaml --outDir src
```

### Compiled spec: openapi.yaml

The compiled version of the OpenAPI spec, for consumption by different tools.

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