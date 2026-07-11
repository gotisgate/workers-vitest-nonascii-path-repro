# workers-vitest-nonascii-path-repro

Minimal reproduction for a Cloudflare Workers SDK issue involving Vitest on Windows when the project workspace path contains non-ASCII characters.

This repository exists solely to reproduce the issue and is not intended to be a production project.

## Environment

- Windows
- Node.js 24.14.1
- npm 11.16.0
- Cloudflare Workers with `@cloudflare/vitest-pool-workers`

## Setup

```sh
npm install
```

## Test

```sh
npm test -- --run
```

## Reproduction

1. Clone or move this repository into a Windows workspace path containing non-ASCII characters, for example `C:\Users\<user>\開発\workers-vitest-nonascii-path-repro`.
2. Run `npm install`.
3. Run `npm test -- --run`.
4. Compare the result with an ASCII-only workspace path. The test suite succeeds from an ASCII path; the issue is reproduced when the Workers runtime or Vitest fails to initialize or execute the generated tests from the non-ASCII path.
