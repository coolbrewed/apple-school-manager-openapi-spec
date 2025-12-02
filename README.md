# Apple School Manager: OpenAPI spec

## About

This is an unofficial, simple OpenAPI spec for the [Apple School Manager API](https://developer.apple.com/documentation/appleschoolmanagerapi). It was created to explore the possibility of generating a client in multiple languages, and is shared as-is.

**Apple School Manager API version:** [v1.3 (2025/11/5)](https://developer.apple.com/documentation/apple-school-and-business-manager-api/apple-school-and-business-manager-api-changelog#13-2025115)

## What's in this repo?

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