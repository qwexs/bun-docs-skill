# bun-docs

Agent skill that routes Bun questions to official documentation instead of a frozen API snapshot.

Bun ships markdown twins for every docs page (`https://bun.com/docs/<path>.md`), a live index (`https://bun.com/llms.txt`), and a type reference generated from `packages/bun-types`. This skill is a thin map plus a fetch protocol.

## Install

```bash
npx skills add qwexs/bun-docs-skill -g -y
```

Or clone into the agent skills directory:

```bash
git clone https://github.com/qwexs/bun-docs-skill.git ~/.agents/skills/bun-docs
```

Works with Grok, Claude Code, Codex, Cursor, and any agent that loads `SKILL.md`.

## What it does

1. Pick the topic from [`references/topics.md`](references/topics.md) (curated official URLs, including release additions missing from the live index).
2. Fetch the markdown page, not the HTML. Section indexes are
   `https://bun.com/docs/<section>.md`, not `.../index.md`.
3. Use [`bun.com/reference`](https://bun.com/reference) or local `@types/bun` for signatures.
4. Use [`bun.com/blog`](https://bun.com/blog) to confirm the latest release,
   then fetch its changelog, including feature and security sections.
   Last verified: [Bun 1.4.3](https://bun.com/blog/bun-v1.4.3), 2026-10-10:
   `bun check` / `--check`, `Bun.FetchSession`, experimental `Bun.ModuleGraph`,
   string-to-code restrictions, `[hashN]` output names, and profile-guided
   bytecode layout / JIT policy for compiled executables.

Source catalog: [`references/sources.md`](references/sources.md).
Known index mismatches and update checklist:
[`references/maintenance.md`](references/maintenance.md).

## Structure

```text
bun-docs/
├── SKILL.md                 # protocol and precedence
└── references/
    ├── maintenance.md       # known broken links and refresh checklist
    ├── sources.md           # canonical vs third-party sources
    └── topics.md            # topic → official URL
```

## Rules the skill enforces

- Do not answer Bun API/CLI questions from memory.
- Official docs win over community snapshots.
- In a Bun project use `bun`, not `node` / `npm` / `npx`.
- Check the installed runtime and project type definitions before recommending release-specific features.
- Prefer Bun-native APIs (`Bun.serve`, `Bun.FetchSession`, `Bun.Image`, `Bun.WebView`, `Bun.markdown`, `Bun.cron`, `Bun.Terminal`, `bun:sqlite`, …) unless the official page says they cannot do the job.
- On Bun 1.4.3+, prefer `bun check` / opt-in `--check` for type checking, with TypeScript 7 semantics and defaults. Keep `tsc` for JavaScript / `.d.ts` emission; `bun check` does not replace the editor's TypeScript language server.
- Mark experimental APIs as experimental (HTTP/2 and HTTP/3 `fetch` clients, `Bun.serve({ http2 })`, `Bun.serve({ http3 })`, `Bun.ModuleGraph`, `install.globalStore`, Android builds). `Bun.ModuleGraph` is not a security sandbox.

## Not official

This is not an Oven / Anthropic project. Pages and URLs come from [bun.com/docs](https://bun.com/docs). If the live index adds a page the map misses, the skill tells the agent to fetch `https://bun.com/llms.txt`.

## License

MIT
