---
name: bun-docs
description: >
  Router to official Bun documentation. Use when writing or reviewing
  Bun/TypeScript code, looking up Bun APIs (Bun.serve, Bun.Image, Bun.file,
  Bun.sql, bun:sqlite, Bun.s3, Bun.redis), CLI (bun install, bun test,
  bun build, bunx), bunfig.toml, Node-to-Bun replacements, or "what's new
  in Bun". Triggers: bun, bun.sh, bun.com, @types/bun, Bun.Image, bun test.
  Use when the user runs /bun-docs.
---

# Bun docs (router)

Do not answer Bun API/CLI questions from memory. Open the official page.

## Protocol

1. Identify the topic (API, CLI, guide, changelog).
2. Pick the URL from `references/topics.md`. Fetch the **markdown** twin:
   `https://bun.com/docs/<path>.md`
3. If the topic is not in the map, fetch the live index:
   `https://bun.com/docs/llms.txt`
4. For exact signatures / overloads: `https://bun.com/reference/bun/<Symbol>`
   or local `node_modules/@types/bun`.
5. For "what landed in X": `https://bun.com/blog/bun-vX.Y.Z` and
   `bun --version`.
6. Cite the URL you used.

Do not fetch `https://bun.com/llms-full.txt` unless the index has no match.

Sources catalog: `references/sources.md`.

## Precedence

1. Official page (`bun.com/docs/...md`)
2. Type reference (`bun.com/reference/...`) or `@types/bun`
3. Release blog (`bun.com/blog/bun-v*`)
4. GitHub issue / Discord — unreleased bugs only

## Hard rules

- In a Bun project (`bun.lock`, `bunfig.toml`, `@types/bun`) use `bun`, not
  `node` / `npm` / `npx`.
- Prefer Bun-native APIs over `express`, `sharp`, `better-sqlite3`, `ioredis`,
  `ws`, `execa` unless the official page says the native API cannot do the job.
- Mark experimental APIs (HTTP/2 and HTTP/3 `fetch` clients, `Bun.serve({ http3 })`,
  `install.globalStore`) as experimental when you recommend them.

## Example

User asks about `Bun.Image`:

1. https://bun.com/docs/runtime/image.md
2. Types: https://bun.com/reference/bun/Image
3. Changelog: https://bun.com/blog/bun-v1.3.14
