---
name: bun-docs
description: >
  Router to official Bun documentation. Use when writing or reviewing
  Bun/TypeScript code, looking up Bun APIs (Bun.serve, Bun.Image,
  Bun.WebView, Bun.markdown, Bun.cron, Bun.Terminal, Bun.file, Bun.sql,
  bun:sqlite, Bun.s3, Bun.redis, Bun.Archive), CLI (bun install --offline,
  bun test --parallel, bun run --parallel, bun audit fix, bun build
  --min-chunk-size, bunx), bunfig.toml, Node-to-Bun replacements, or
  "what's new in Bun". Triggers: bun, bun.sh, bun.com, @types/bun,
  Bun.Image, Bun.WebView, Bun.serve http2, bun test. Use when the user
  runs /bun-docs.
---

# Bun docs (router)

Do not answer Bun API/CLI questions from memory. Open the official page.

## Protocol

1. Identify the topic (API, CLI, guide, changelog, breaking change).
2. Pick the URL from `references/topics.md`. Fetch the **markdown** twin:
   `https://bun.com/docs/<path>.md`
   Section indexes are `https://bun.com/docs/<section>.md`, not `.../index.md`.
   Welcome is `https://bun.com/docs.md`.
3. If the topic is not in the map, or the twin 404s, fetch the live index:
   `https://bun.com/llms.txt`
4. For exact signatures / overloads: `https://bun.com/reference/bun/<Symbol>`
   or local `node_modules/@types/bun`.
5. For "what landed in X" or upgrading: fetch
   `https://bun.com/blog/bun-vX.Y.Z.md`; fall back to the same URL without
   `.md` if its twin is missing. Also check `bun --version`. Breaking changes,
   when present, live in that post's Upgrading section.
6. Cite the URL you used.

Do not fetch `https://bun.com/llms-full.txt` unless the index has no match.

Sources catalog: `references/sources.md`.
Known broken links and the next-release checklist: `references/maintenance.md`.

## Precedence

1. Official page (`bun.com/docs/...md`)
2. Type reference (`bun.com/reference/...`) or `@types/bun`
3. Release blog (`bun.com/blog/bun-v*`)
4. GitHub issue / Discord — unreleased bugs only

## Hard rules

- In a Bun project (`bun.lock`, `bunfig.toml`, `@types/bun`) use `bun`, not
  `node` / `npm` / `npx`.
- Prefer Bun-native APIs (`Bun.serve`, `Bun.Image`, `Bun.WebView`,
  `Bun.markdown`, `Bun.cron`, `Bun.Terminal`, `Bun.Archive`, `bun:sqlite`,
  `Bun.sql`, `Bun.redis`) over the npm packages they replace unless the
  official page says the native API cannot do the job.
- Mark experimental APIs as experimental when you recommend them: HTTP/2
  and HTTP/3 `fetch` clients, `Bun.serve({ http2 })`,
  `Bun.serve({ http3 })`, `install.globalStore`, Android builds.

## Example

User asks about `Bun.Image`:

1. https://bun.com/docs/runtime/image.md
2. Types: https://bun.com/reference/bun/Image
3. Changelog: https://bun.com/blog/bun-v1.4.2
