# Maintenance notes

Use this file when refreshing the topic map for a new Bun release. Recheck every
observation: these are current site behaviors, not permanent URL rules.

## Known `llms.txt` index mismatches

Checked 2026-09-05 against https://bun.com/llms.txt.

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

## Redirects and release twins to watch

- Guide pages under `https://bun.com/docs/guides/<path>.md` currently redirect
  to `https://bun.com/guides/<path>.md` and return markdown. On the next broad
  refresh, compare the final canonical URLs before deciding whether to update
  the map in bulk.
- `https://bun.com/blog/bun-v1.4.1.md` and `bun-v1.4.2.md` work, but
  `https://bun.com/blog/bun-v1.4.0.md` does not. Test each release-post twin;
  do not infer support from another version.
- The Bun 1.4.0 HTML URL redirects to `https://bun.com/blog/bun-v1.4`.
  Preserve version-specific links only while their anchors still resolve.

## Next release refresh

1. Confirm releases and dates with
   `gh release list --repo oven-sh/bun` and `gh release view bun-vX.Y.Z`.
2. Fetch `https://bun.com/blog/bun-vX.Y.Z.md`; fall back to HTML on 404.
3. Compare the `docs/**` trees between the previous and new Git tags with
   `gh api repos/oven-sh/bun/compare/<old>...<new>`.
4. Fetch https://bun.com/llms.txt and compare its docs URLs with
   `references/topics.md`. Normalize only the five known index mismatches above.
5. Add keywords for new APIs, flags, configuration keys, and compatibility
   changes even when Bun only modified an existing docs page.
6. Check exact type-reference URLs and the release post's experimental and
   upgrading language. Patch releases may have no Upgrading section.
7. GET every literal `bun.com` URL with redirects enabled. Record 4xx responses,
   unexpected final URLs, and non-markdown docs responses.
8. Verify every release fragment against a real heading ID, then update the
   version and verification date in `references/sources.md`.

At the 1.4.2 refresh, the pre-note catalog had 357 unique literal `bun.com`
URL targets; all returned below 400 after redirects, and all 24 release
fragments resolved. Separate direct probes of the five `/index.md` URLs above
produced the failures documented here.
