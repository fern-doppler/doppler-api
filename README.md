# Doppler API

Tagging a release on this repository will update the:

- [TypeScript SDK repo](https://github.com/fern-doppler/doppler-node)
- [OpenAPI description repo](https://github.com/fern-doppler/doppler-openapi)
- [Postman collection repo](https://github.com/fern-doppler/doppler-postman)
- _More SDKs to come..._

## What is in this repository?

This repository contains

- Doppler's Fern API Definition which lives in the [definition](./fern/api/definition/) folder
- Generators (see [generators.yml](./fern/api/generators.yml))

## What is in the API Definition?

The API Definition contains information about what endpoints, types, and errors are used in the API. The definition is broken into smaller files such as [workplace.yml](fern/api/definition/workplace.yml) and [projects.yml](fern/api/definition/projects.yml).

In order to make sure that the definition is valid, you can use the Fern CLI.

```bash
npm install -g fern-api # Installs CLI
fern check # Checks if the definition is valid
```

## What are Generators?

Generators read in your API Definition and output files or code (i.e. the TypeScript SDK Generator) and are tracked in [generators.yml](./fern/api/generators.yml).

To trigger the generators run:

```bash
fern release <version>
```

This command currently runs in a GitHub workflow (see [ci.yml](.github/workflows/ci.yml#L32))
