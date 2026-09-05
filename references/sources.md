# Bun sources

Live official sources first. Community snapshots last.

## Canonical (fetch these)

| Source | URL | Use for |
|---|---|---|
| Docs index (llms.txt) | https://bun.com/llms.txt | Discover the right page. `/docs/llms.txt` redirects here. |
| Docs page (markdown) | `https://bun.com/docs/<path>.md` | How-to, limits, examples. Always append `.md`. |
| Welcome | https://bun.com/docs.md | Index of the docs site (`/docs/index.md` 404s). |
| Type reference | https://bun.com/reference | Generated from `packages/bun-types`. Symbol: `/reference/bun/Image` |
| Release blog | https://bun.com/blog | Changelog per version. Latest: https://bun.com/blog/bun-v1.4.2 |
| Bun 1.4.2 | https://bun.com/blog/bun-v1.4.2.md | Latest patch; fixes 1.4.1 regressions and compatibility bugs |
| Bun 1.4.1 | https://bun.com/blog/bun-v1.4.1.md | HTTP/2 server, offline install, bytecode/build and runtime additions |
| Bun 1.4.0 release notes | https://bun.com/blog/release-notes/bun-v1.4.0 | Per-PR notes that the 1.4 post links to |
| Rust rewrite | https://bun.com/blog/bun-in-rust | Why/how Bun moved from Zig to Rust |
| Node.js test suite | https://bun.com/node-test-suite | Live pass/fail vs Node's own tests |
| GitHub docs source | https://github.com/oven-sh/bun/tree/main/docs | `.mdx` sources if the site `.md` is stale or missing |
| Type definitions | https://github.com/oven-sh/bun/tree/main/packages/bun-types | Ground truth for the `Bun` global. Locally: `node_modules/@types/bun` / `bun-types` |
| Node compat matrix | https://bun.com/docs/runtime/nodejs-compat.md | What Node APIs exist / are partial |
| Feedback | https://bun.com/docs/feedback.md | Where to file bugs |

Full dump (avoid unless the index has no match): https://bun.com/llms-full.txt

## How to fetch a page

```
https://bun.com/docs.md
https://bun.com/docs/runtime.md
https://bun.com/docs/runtime/image.md
https://bun.com/docs/pm/cli/install.md
https://bun.com/docs/bundler.md
https://bun.com/docs/test.md
https://bun.com/guides.md
https://bun.com/reference/bun/Image
https://bun.com/blog/bun-v1.4.2.md
https://bun.com/blog/bun-v1.4.1.md
```

Human URL without `.md` also works; prefer `.md` for agents. Release-post
markdown twins are not universal, so fall back to the HTML post on a 404.

Section indexes are `https://bun.com/docs/<section>.md`, not `.../index.md`.
`/docs/runtime/index.md`, `/docs/bundler/index.md`, `/docs/test/index.md`,
and `/docs/index.md` 404. If a twin 404s, retry without `/index`, then
`https://bun.com/llms.txt`.

`llms.txt` can list stale twins. The topic map is the working URL. See
`maintenance.md` for known mismatches and the next-release verification steps.

## Version

- Runtime: `bun --version` (topic map last verified against 1.4.2, 2026-09-05)
- Releases: `gh release list --repo oven-sh/bun`
- Tag: `bun-vX.Y.Z` → blog `https://bun.com/blog/bun-vX.Y.Z`
- Breaking changes: that post's Upgrading section, when present

## Official adjacent

| Source | URL | Use for |
|---|---|---|
| GitHub | https://github.com/oven-sh/bun | Issues, source, discussions |
| GitHub Actions | https://github.com/oven-sh/setup-bun | CI install |
| Docker | https://github.com/oven-sh/docker | Official images |
| Homebrew tap | https://github.com/oven-sh/homebrew-bun | macOS install |
| Awesome Bun | https://github.com/oven-sh/awesome-bun | Ecosystem list (not API docs) |
| Discord | https://bun.com/discord | Unreleased / "is this a bug" |
| Roadmap | https://bun.com/docs/project/roadmap.md | Planned work |

## Third-party (optional, never canonical)

| Source | URL | Note |
|---|---|---|
| Context7 | https://context7.com/websites/bun_sh | Live crawl of bun.sh/docs. Useful if HTTP to bun.com fails. |
| bun-doc-mcp | https://github.com/ghoulr/bun-doc-mcp | Version-matched docs MCP. Last npm publish 2025-09. |
| bun-mcp-server | https://github.com/chikingsley/bun-mcp-server | Fork with FTS search. 0 stars. |
| jarle/bun-skills | https://github.com/jarle/bun-skills | 306-page dump of bun.sh, frozen 2026-02. Misses 1.4. |

Do not treat Discord, awesome-bun, or community skills as API truth.
