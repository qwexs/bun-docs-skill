# Maintenance notes

Use this file when refreshing the topic map for a new Bun release. Recheck every
observation: these are current site behaviors, not permanent URL rules.

## Known `llms.txt` index mismatches

Checked 2026-10-10 against https://bun.com/llms.txt and direct GET requests.

| URL listed by `llms.txt` | Current result | Working markdown URL |
|---|---|---|
| https://bun.com/docs/index.md | 404 | https://bun.com/docs.md |
| https://bun.com/docs/runtime/index.md | 404 | https://bun.com/docs/runtime.md |
| https://bun.com/docs/bundler/index.md | 404 | https://bun.com/docs/bundler.md |
| https://bun.com/docs/test/index.md | 404 | https://bun.com/docs/test.md |
| https://bun.com/docs/guides/index.md | 308 to `/guides/index.md`, then 404 | https://bun.com/guides.md |

Keep the working forms in `references/topics.md` until direct requests prove a
new form works. Do not replace them only because `llms.txt` still lists
`/index.md`.

There is no confirmed Bun documentation fix date or migration notice for these
links. Do not assume the index will be repaired in the next release.

## Release pages missing from `llms.txt`

At the 1.4.3 refresh, the live index still listed the same 319 markdown docs
URLs as the previous map (after normalizing the five index mismatches above).
Three docs pages were added between tags `bun-v1.4.2` and `bun-v1.4.3`, all
confirmed to return markdown with HTTP 200 but absent from `llms.txt`:

- `bun check`: https://bun.com/docs/runtime/check.md
- String-to-code restrictions: https://bun.com/docs/runtime/code-generation-from-strings.md
- Experimental `Bun.ModuleGraph`: https://bun.com/docs/runtime/module-graph.md

Keep these explicit routes even while the index omits them. When a new API or
flag is not in the index, inspect the release post and version-tagged docs
source rather than assuming the feature is undocumented.

## Redirects and release twins to watch

- Guide pages under `https://bun.com/docs/guides/<path>.md` currently redirect
  to `https://bun.com/guides/<path>.md` and return markdown. On the next broad
  refresh, compare the final canonical URLs before deciding whether to update
  the map in bulk.
- `https://bun.com/blog/bun-v1.4.1.md`, `bun-v1.4.2.md`, and `bun-v1.4.3.md`
  work, but `https://bun.com/blog/bun-v1.4.0.md` still returns 404. Test each
  release-post twin; do not infer support from another version.
- The Bun 1.4.0 HTML URL redirects to `https://bun.com/blog/bun-v1.4`.
  Preserve version-specific links only while their anchors still resolve.

## Next release refresh

1. Confirm releases and dates with
   `gh release list --repo oven-sh/bun` and `gh release view bun-vX.Y.Z`.
2. Fetch `https://bun.com/blog/bun-vX.Y.Z.md`; fall back to HTML on 404.
3. Compare the `docs/**` trees between the previous and new Git tags. Use
   `gh api repos/oven-sh/bun/compare/<old>...<new>` for patches, but it lists
   at most 300 changed files. For a complete docs diff, resolve each tag with
   `gh api repos/oven-sh/bun/git/trees/<tag>`, then fetch the `docs` subtree
   SHA with `gh api repos/oven-sh/bun/git/trees/<docs-sha>?recursive=1` and
   compare paths and blob SHAs. Check the response's `truncated` field.
4. Fetch https://bun.com/llms.txt and compare its docs URLs with
   `references/topics.md`. Normalize only the five known index mismatches
   above; also check release-added pages that the index may not list yet.
5. Add keywords for new APIs, flags, configuration keys, and compatibility
   changes even when Bun only modified an existing docs page.
6. Check exact type-reference URLs and the release post's experimental and
   upgrading language. Patch releases may have no Upgrading section: also
   inspect feature, security, and bugfix sections for behavior changes.
7. GET each concrete catalog `bun.com` URL with redirects enabled. Exclude
   templates and trailing prose punctuation; probe known broken examples
   separately. For `llms-full.txt`, use HEAD instead of downloading the full
   dump just to validate a link. Record 4xx responses, unexpected final URLs,
   and non-markdown docs responses.
8. Verify every release fragment against a real heading ID, then update the
   version and verification date in `references/sources.md`.

## 1.4.3 refresh cautions

- `bun check` uses TypeScript 7 semantics and defaults regardless of the
  installed `typescript` package. It only checks: keep `tsc` for JavaScript
  or `.d.ts` emission. It does not replace the editor's TypeScript language
  server.
- `Bun.ModuleGraph` is experimental and is not a security sandbox.
- Non-2xx proxy CONNECT responses now reject `fetch()` with
  `ERR_PROXY_TUNNEL` instead of resolving with the proxy response.
- `--disallow-code-generation-from-strings` is now enforced rather than
  ignored. Bun-only `=strict` also blocks other string-to-code paths.
- An offline install's cache must be warmed for at least the same packages
  on the same platform; `--production` and `--omit` leave groups uncached.
- The release post has an upgrade command but no dedicated Upgrading section.

The complete tagged docs-subtree comparison found three added pages and no
removed pages (387 → 390 files). The compare API returned 300 changed files
for this release, so its file list alone is not a complete repository diff.

## Verification (2026-10-10)

- Confirmed stable tag `bun-v1.4.3` and local runtime `1.4.3`.
- Parsed `SKILL.md` frontmatter: valid name and a 743-character description
  (within the 1024-character limit). Local README links resolve.
- The working-link catalog (`SKILL.md`, `README.md`, `sources.md`, `topics.md`)
  has 416 unique literal `bun.com` URLs, covering 370 HTTP request targets.
  All returned below 400 after redirects, and all 47 release fragments resolved.
- All 322 mapped docs URLs return markdown. The map covers all 319 normalized
  live-index docs URLs plus the three release additions above.
- All 190 guide-page redirects went from `/docs/guides/` to `/guides/` as
  expected; no unexpected catalog redirects or non-markdown docs responses.
- Separate GET probes confirmed the five broken `/index.md` URLs and the
  missing 1.4.0 release-post twin documented above; they are not working routes.
