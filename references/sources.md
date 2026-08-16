# Bun sources

Live official sources first. Community snapshots last.

## Canonical (fetch these)

| Source | URL | Use for |
|---|---|---|
| Docs index (llms.txt) | https://bun.com/docs/llms.txt | Discover the right page. Same file at https://bun.com/llms.txt |
| Docs page (markdown) | `https://bun.com/docs/<path>.md` | How-to, limits, examples. Always append `.md`. |
| Guides index | https://bun.com/docs/guides/index.md | Short recipes (HTTP, files, install, test, deploy) |
| Type reference | https://bun.com/reference | Generated from `packages/bun-types`. Symbol: `/reference/bun/Image` |
| Release blog | https://bun.com/blog | Changelog per version. Latest: https://bun.com/blog/bun-v1.3.14 |
| GitHub docs source | https://github.com/oven-sh/bun/tree/main/docs | `.mdx` sources if the site `.md` is stale or missing |
| Type definitions | https://github.com/oven-sh/bun/tree/main/packages/bun-types | Ground truth for the `Bun` global. Locally: `node_modules/@types/bun` / `bun-types` |
| Node compat matrix | https://bun.com/docs/runtime/nodejs-compat.md | What Node APIs exist / are partial |
| Feedback | https://bun.com/docs/feedback.md | Where to file bugs |

Full dump (avoid unless the index has no match): https://bun.com/llms-full.txt

## How to fetch a page

```
https://bun.com/docs/runtime/image.md
https://bun.com/docs/pm/cli/install.md
https://bun.com/docs/guides/http/simple.md
https://bun.com/reference/bun/Image
https://bun.com/blog/bun-v1.3.14
```

Human URL without `.md` also works; prefer `.md` for agents.

## Version

- Runtime: `bun --version` (topic map last verified against 1.3.14)
- Releases: `gh release list --repo oven-sh/bun`
- Tag: `bun-vX.Y.Z` → blog `https://bun.com/blog/bun-vX.Y.Z`

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
| jarle/bun-skills | https://github.com/jarle/bun-skills | 306-page dump of bun.sh, frozen 2026-02. |

Do not treat Discord, awesome-bun, or community skills as API truth.
