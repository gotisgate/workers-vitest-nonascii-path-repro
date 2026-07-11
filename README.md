# workers-vitest-nonascii-path-repro
<<<<<<< HEAD
This repository exists solely as a minimal reproduction for a Cloudflare Workers SDK issue.
It is not intended to be a production project.
=======

Minimal reproduction for a Cloudflare Workers SDK issue involving Vitest on Windows when the project workspace path contains non-ASCII characters.

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

1. Clone or move this repository into a Windows path containing non-ASCII characters, for example `C:\Users\<user>\開発\workers-vitest-nonascii-path-repro`.
2. Run `npm install`.
3. Run `npm test -- --run`.
4. Observe whether the Workers runtime and Vitest initialize and execute the generated tests.
>>>>>>> 320d77b (chore: initialize minimal Cloudflare Workers reproduction project)
