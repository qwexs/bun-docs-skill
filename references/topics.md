# Topic → official page

Prefix for docs: `https://bun.com/docs/`. Always fetch the `.md` twin.
Section indexes: `https://bun.com/docs/<section>.md` (not `.../index.md`).
Welcome: `https://bun.com/docs.md`. Live index if a page is missing:
https://bun.com/llms.txt

## Start

| Topic | URL |
|---|---|
| Welcome | https://bun.com/docs.md |
| Install | https://bun.com/docs/installation.md |
| Quickstart | https://bun.com/docs/quickstart.md |
| TypeScript | https://bun.com/docs/typescript.md |
| TypeScript 6 / 7 (`types: ["bun"]`) | https://bun.com/docs/typescript-6.md |
| bun init | https://bun.com/docs/runtime/templating/init.md |
| bun create | https://bun.com/docs/runtime/templating/create.md |
| bunfig.toml / `install.offline` / `install.prefer` | https://bun.com/docs/runtime/bunfig.md |
| Feedback | https://bun.com/docs/feedback.md |

## Runtime

| Topic | URL |
|---|---|
| Runtime overview / `bun run` | https://bun.com/docs/runtime.md |
| `bun run --parallel` / `--sequential` | https://bun.com/docs/runtime.md |
| Watch / `--hot` | https://bun.com/docs/runtime/watch-mode.md |
| Debugger | https://bun.com/docs/runtime/debugger.md |
| REPL | https://bun.com/docs/runtime/repl.md |
| File types / loaders | https://bun.com/docs/runtime/file-types.md |
| Module resolution | https://bun.com/docs/runtime/module-resolution.md |
| JSX | https://bun.com/docs/runtime/jsx.md |
| Auto-install | https://bun.com/docs/runtime/auto-install.md |
| Plugins (runtime) | https://bun.com/docs/runtime/plugins.md |
| File System Router | https://bun.com/docs/runtime/file-system-router.md |
| Environment variables / `--env-file` pipes, FIFOs, stdin | https://bun.com/docs/runtime/environment-variables.md |
| Console | https://bun.com/docs/runtime/console.md |
| Globals | https://bun.com/docs/runtime/globals.md |
| Bun APIs overview | https://bun.com/docs/runtime/bun-apis.md |
| Web APIs | https://bun.com/docs/runtime/web-apis.md |
| Node.js compatibility | https://bun.com/docs/runtime/nodejs-compat.md |
| Utils (`stringWidth`, `wrapAnsi`, `stripANSI`, `sliceAnsi`) | https://bun.com/docs/runtime/utils.md |

## HTTP & networking

| Topic | URL |
|---|---|
| `Bun.serve` | https://bun.com/docs/runtime/http/server.md |
| HTTP/2 (`Bun.serve({ http2 })`, experimental) | https://bun.com/docs/runtime/http/server.md |
| HTTP/3 (`Bun.serve({ http3 })`, experimental) | https://bun.com/docs/runtime/http/server.md |
| Routing | https://bun.com/docs/runtime/http/routing.md |
| Static files (`{ dir }`) | https://bun.com/docs/runtime/http/routing.md |
| Cookies (HTTP) | https://bun.com/docs/runtime/http/cookies.md |
| Cookies (API) | https://bun.com/docs/runtime/cookies.md |
| TLS | https://bun.com/docs/runtime/http/tls.md |
| Error handling | https://bun.com/docs/runtime/http/error-handling.md |
| Metrics | https://bun.com/docs/runtime/http/metrics.md |
| WebSockets / client `pause()`, `resume()`, `isPaused` | https://bun.com/docs/runtime/http/websockets.md |
| Server WebSocket `binaryType = "blob"` | https://bun.com/reference/bun/ServerWebSocket/binaryType |
| `fetch` / HTTP/2 / HTTP/3 | https://bun.com/docs/runtime/networking/fetch.md |
| TCP | https://bun.com/docs/runtime/networking/tcp.md |
| UDP | https://bun.com/docs/runtime/networking/udp.md |
| DNS | https://bun.com/docs/runtime/networking/dns.md |

## Data, files, processes

| Topic | URL |
|---|---|
| File I/O / streaming `Bun.write(path, Response)` | https://bun.com/docs/runtime/file-io.md |
| Streams | https://bun.com/docs/runtime/streams.md |
| Binary data | https://bun.com/docs/runtime/binary-data.md |
| Archive (`Bun.Archive`) | https://bun.com/docs/runtime/archive.md |
| SQL (`Bun.sql`) | https://bun.com/docs/runtime/sql.md |
| `bun:sqlite` | https://bun.com/docs/runtime/sqlite.md |
| S3 | https://bun.com/docs/runtime/s3.md |
| Redis | https://bun.com/docs/runtime/redis.md |
| Shell (`Bun.$`) | https://bun.com/docs/runtime/shell.md |
| Spawn | https://bun.com/docs/runtime/child-process.md |
| Terminal / PTY (`Bun.Terminal`) | https://bun.com/docs/runtime/child-process.md |
| Workers | https://bun.com/docs/runtime/workers.md |
| Image (`Bun.Image`) | https://bun.com/docs/runtime/image.md |
| Hashing / passwords | https://bun.com/docs/runtime/hashing.md |
| `node:crypto` Argon2 | https://bun.com/reference/node/crypto/argon2 |
| Glob | https://bun.com/docs/runtime/glob.md |
| Semver | https://bun.com/docs/runtime/semver.md |
| Color | https://bun.com/docs/runtime/color.md |
| HTMLRewriter | https://bun.com/docs/runtime/html-rewriter.md |

## Parsing & extras

| Topic | URL |
|---|---|
| Markdown | https://bun.com/docs/runtime/markdown.md |
| JSON5 | https://bun.com/docs/runtime/json5.md |
| JSONC (`Bun.JSONC`, `.jsonc`) | https://bun.com/docs/runtime/file-types.md |
| JSONL | https://bun.com/docs/runtime/jsonl.md |
| YAML | https://bun.com/docs/runtime/yaml.md |
| TOML | https://bun.com/docs/runtime/toml.md |
| XML | https://bun.com/docs/runtime/xml.md |
| WebView | https://bun.com/docs/runtime/webview.md |
| Cron | https://bun.com/docs/runtime/cron.md |
| CSRF | https://bun.com/docs/runtime/csrf.md |
| Secrets | https://bun.com/docs/runtime/secrets.md |
| Transpiler | https://bun.com/docs/runtime/transpiler.md |
| FFI | https://bun.com/docs/runtime/ffi.md |
| C compiler / `--no-ffi-cc` | https://bun.com/docs/runtime/c-compiler.md |
| Node-API | https://bun.com/docs/runtime/node-api.md |

## Package manager

| Topic | URL |
|---|---|
| bun install / `--offline` / `--prefer-offline` | https://bun.com/docs/pm/cli/install.md |
| bun add | https://bun.com/docs/pm/cli/add.md |
| bun add `--catalog` / `--filter` | https://bun.com/docs/pm/cli/add.md |
| bun remove | https://bun.com/docs/pm/cli/remove.md |
| bun update | https://bun.com/docs/pm/cli/update.md |
| bun dedupe | https://bun.com/docs/pm/cli/dedupe.md |
| bun prune | https://bun.com/docs/pm/cli/prune.md |
| bunx | https://bun.com/docs/pm/bunx.md |
| bun publish | https://bun.com/docs/pm/cli/publish.md |
| bun outdated | https://bun.com/docs/pm/cli/outdated.md |
| bun why | https://bun.com/docs/pm/cli/why.md |
| bun audit / `bun audit fix` | https://bun.com/docs/pm/cli/audit.md |
| bun info | https://bun.com/docs/pm/cli/info.md |
| bun link | https://bun.com/docs/pm/cli/link.md |
| bun pm | https://bun.com/docs/pm/cli/pm.md |
| bun pm diff | https://bun.com/docs/pm/cli/pm.md |
| bun pm licenses | https://bun.com/docs/pm/cli/pm.md |
| bun patch | https://bun.com/docs/pm/cli/patch.md |
| bun --filter | https://bun.com/docs/pm/filter.md |
| Workspaces / `selfContained` / `hoistingLimits` | https://bun.com/docs/pm/workspaces.md |
| Catalogs | https://bun.com/docs/pm/catalogs.md |
| Isolated installs | https://bun.com/docs/pm/isolated-installs.md |
| Global cache | https://bun.com/docs/pm/global-cache.md |
| Global virtual store | https://bun.com/docs/pm/global-store.md |
| Lockfile | https://bun.com/docs/pm/lockfile.md |
| Lifecycle / trustedDependencies | https://bun.com/docs/pm/lifecycle.md |
| Scopes and registries | https://bun.com/docs/pm/scopes-registries.md |
| Overrides | https://bun.com/docs/pm/overrides.md |
| Security Scanner API | https://bun.com/docs/pm/security-scanner-api.md |
| .npmrc | https://bun.com/docs/pm/npmrc.md |

## Bundler

| Topic | URL |
|---|---|
| Bundler | https://bun.com/docs/bundler.md |
| `--metafile-md` | https://bun.com/docs/bundler.md |
| `--min-chunk-size` / `minChunkSize` | https://bun.com/docs/bundler.md |
| Module preload / `--no-module-preload` / `modulePreload` | https://bun.com/docs/bundler.md |
| Split `require()` / `--no-split-require` / `splitRequire` | https://bun.com/docs/bundler.md |
| Fullstack dev server | https://bun.com/docs/bundler/fullstack.md |
| Hot reloading | https://bun.com/docs/bundler/hot-reloading.md |
| HTML & static sites | https://bun.com/docs/bundler/html-static.md |
| Standalone HTML | https://bun.com/docs/bundler/standalone-html.md |
| CSS | https://bun.com/docs/bundler/css.md |
| Loaders | https://bun.com/docs/bundler/loaders.md |
| Single-file executable | https://bun.com/docs/bundler/executables.md |
| Plugins (bundler) | https://bun.com/docs/bundler/plugins.md |
| Macros | https://bun.com/docs/bundler/macros.md |
| Bytecode / `--bytecode-depth` / `bytecodeDepth` | https://bun.com/docs/bundler/bytecode.md |
| Minifier | https://bun.com/docs/bundler/minifier.md |
| esbuild migrate | https://bun.com/docs/bundler/esbuild.md |

## Test runner

| Topic | URL |
|---|---|
| bun test | https://bun.com/docs/test.md |
| Writing tests | https://bun.com/docs/test/writing-tests.md |
| Configuration | https://bun.com/docs/test/configuration.md |
| Runtime behavior | https://bun.com/docs/test/runtime-behavior.md |
| Finding tests | https://bun.com/docs/test/discovery.md |
| Parallel / isolate / shard | https://bun.com/docs/test/parallel.md |
| Lifecycle hooks | https://bun.com/docs/test/lifecycle.md |
| Mocks | https://bun.com/docs/test/mocks.md |
| Snapshots | https://bun.com/docs/test/snapshots.md |
| Dates and times | https://bun.com/docs/test/dates-times.md |
| DOM testing | https://bun.com/docs/test/dom.md |
| Coverage | https://bun.com/docs/test/code-coverage.md |
| Reporters | https://bun.com/docs/test/reporters.md |

## Project

| Topic | URL |
|---|---|
| Roadmap | https://bun.com/docs/project/roadmap.md |
| Benchmarking | https://bun.com/docs/project/benchmarking.md |
| Contributing | https://bun.com/docs/project/contributing.md |
| Building Windows | https://bun.com/docs/project/building-windows.md |
| Bindgen | https://bun.com/docs/project/bindgen.md |
| License | https://bun.com/docs/project/license.md |

## Type reference

Generated from `packages/bun-types`. Search on https://bun.com/reference

| Symbol | URL |
|---|---|
| `Bun` | https://bun.com/reference/bun |
| `Bun.Image` | https://bun.com/reference/bun/Image |
| `Bun.WebView` | https://bun.com/reference/bun/WebView |
| `Bun.Terminal` | https://bun.com/reference/bun/Terminal |
| `Bun.WebSocket.pause()` / `resume()` / `isPaused` | https://bun.com/reference/bun/WebSocket |
| `Bun.cron` | https://bun.com/reference/bun/cron |
| `Bun.markdown` | https://bun.com/reference/bun/markdown |
| `Bun.Archive` | https://bun.com/reference/bun/Archive |
| `Bun.BuildConfig.minChunkSize` | https://bun.com/reference/bun/BuildConfig/minChunkSize |
| `Bun.BuildConfig.bytecodeDepth` | https://bun.com/reference/bun/BuildConfig/bytecodeDepth |
| `Bun.JSON5` | https://bun.com/reference/bun/JSON5 |
| `Bun.JSONC` | https://bun.com/reference/bun/JSONC |
| `Bun.JSONL` | https://bun.com/reference/bun/JSONL |
| `Bun.XML` | https://bun.com/reference/bun/XML |
| `bun:sqlite` | https://bun.com/reference/bun/sqlite |
| `bun:test` | https://bun.com/reference/bun/test |
| `bun:ffi` | https://bun.com/reference/bun/ffi |
| `bun:jsc` | https://bun.com/reference/bun/jsc |
| `bun:bundle` | https://bun.com/reference/bun/bundle |
| Globals | https://bun.com/reference/globals |

Node modules: `https://bun.com/reference/node/<module>` (e.g. `fs`, `http`, `tls`, `quic`).
Argon2: https://bun.com/reference/node/crypto/argon2 and
https://bun.com/reference/node/crypto/argon2Sync.

## Guides

Index: https://bun.com/guides.md

### Deploy

| Topic | URL |
|---|---|
| Vercel | https://bun.com/docs/guides/deployment/vercel.md |
| Railway | https://bun.com/docs/guides/deployment/railway.md |
| Render | https://bun.com/docs/guides/deployment/render.md |
| AWS Lambda | https://bun.com/docs/guides/deployment/aws-lambda.md |
| DigitalOcean | https://bun.com/docs/guides/deployment/digital-ocean.md |
| Google Cloud Run | https://bun.com/docs/guides/deployment/google-cloud-run.md |

### Runtime recipes

| Topic | URL |
|---|---|
| Install TypeScript declarations | https://bun.com/docs/guides/runtime/typescript.md |
| tsconfig paths | https://bun.com/docs/guides/runtime/tsconfig-paths.md |
| VS Code debugger | https://bun.com/docs/guides/runtime/vscode-debugger.md |
| Web debugger | https://bun.com/docs/guides/runtime/web-debugger.md |
| V8 heap snapshot | https://bun.com/docs/guides/runtime/heap-snapshot.md |
| `--define` constants | https://bun.com/docs/guides/runtime/build-time-constants.md |
| Replace static globals | https://bun.com/docs/guides/runtime/define-constant.md |
| GitHub Actions | https://bun.com/docs/guides/runtime/cicd.md |
| Codesign macOS executable | https://bun.com/docs/guides/runtime/codesign-macos-executable.md |
| Shell command | https://bun.com/docs/guides/runtime/shell.md |
| Timezone | https://bun.com/docs/guides/runtime/timezone.md |
| Set env | https://bun.com/docs/guides/runtime/set-env.md |
| Read env | https://bun.com/docs/guides/runtime/read-env.md |
| Delete file | https://bun.com/docs/guides/runtime/delete-file.md |
| Delete directory | https://bun.com/docs/guides/runtime/delete-directory.md |
| Import JSON | https://bun.com/docs/guides/runtime/import-json.md |
| Import TOML | https://bun.com/docs/guides/runtime/import-toml.md |
| Import YAML | https://bun.com/docs/guides/runtime/import-yaml.md |
| Import JSON5 | https://bun.com/docs/guides/runtime/import-json5.md |
| Import XML | https://bun.com/docs/guides/runtime/import-xml.md |
| Import HTML as text | https://bun.com/docs/guides/runtime/import-html.md |

### Utils

| Topic | URL |
|---|---|
| Upgrade Bun | https://bun.com/docs/guides/util/upgrade.md |
| Detect Bun | https://bun.com/docs/guides/util/detect-bun.md |
| Current version | https://bun.com/docs/guides/util/version.md |
| Hash a password | https://bun.com/docs/guides/util/hash-a-password.md |
| UUID | https://bun.com/docs/guides/util/javascript-uuid.md |
| Base64 | https://bun.com/docs/guides/util/base64.md |
| gzip | https://bun.com/docs/guides/util/gzip.md |
| deflate | https://bun.com/docs/guides/util/deflate.md |
| Escape HTML | https://bun.com/docs/guides/util/escape-html.md |
| Deep equals | https://bun.com/docs/guides/util/deep-equals.md |
| Sleep | https://bun.com/docs/guides/util/sleep.md |
| file URL → path | https://bun.com/docs/guides/util/file-url-to-path.md |
| path → file URL | https://bun.com/docs/guides/util/path-to-file-url.md |
| `Bun.which` | https://bun.com/docs/guides/util/which-path-to-executable-bin.md |
| `import.meta.dir` | https://bun.com/docs/guides/util/import-meta-dir.md |
| `import.meta.file` | https://bun.com/docs/guides/util/import-meta-file.md |
| `import.meta.path` | https://bun.com/docs/guides/util/import-meta-path.md |
| Is entrypoint | https://bun.com/docs/guides/util/entrypoint.md |
| `Bun.main` | https://bun.com/docs/guides/util/main.md |

### Ecosystem

| Topic | URL |
|---|---|
| Astro | https://bun.com/docs/guides/ecosystem/astro.md |
| Discord.js | https://bun.com/docs/guides/ecosystem/discordjs.md |
| Docker | https://bun.com/docs/guides/ecosystem/docker.md |
| Drizzle | https://bun.com/docs/guides/ecosystem/drizzle.md |
| Gel | https://bun.com/docs/guides/ecosystem/gel.md |
| Elysia | https://bun.com/docs/guides/ecosystem/elysia.md |
| Express | https://bun.com/docs/guides/ecosystem/express.md |
| Hono | https://bun.com/docs/guides/ecosystem/hono.md |
| Mongoose | https://bun.com/docs/guides/ecosystem/mongoose.md |
| Neon + Drizzle | https://bun.com/docs/guides/ecosystem/neon-drizzle.md |
| Neon serverless | https://bun.com/docs/guides/ecosystem/neon-serverless-postgres.md |
| Next.js | https://bun.com/docs/guides/ecosystem/nextjs.md |
| Nuxt | https://bun.com/docs/guides/ecosystem/nuxt.md |
| PM2 | https://bun.com/docs/guides/ecosystem/pm2.md |
| Prisma | https://bun.com/docs/guides/ecosystem/prisma.md |
| Prisma Postgres | https://bun.com/docs/guides/ecosystem/prisma-postgres.md |
| Qwik | https://bun.com/docs/guides/ecosystem/qwik.md |
| React | https://bun.com/docs/guides/ecosystem/react.md |
| Remix | https://bun.com/docs/guides/ecosystem/remix.md |
| TanStack Start | https://bun.com/docs/guides/ecosystem/tanstack-start.md |
| Sentry | https://bun.com/docs/guides/ecosystem/sentry.md |
| SolidStart | https://bun.com/docs/guides/ecosystem/solidstart.md |
| SSR React | https://bun.com/docs/guides/ecosystem/ssr-react.md |
| SvelteKit | https://bun.com/docs/guides/ecosystem/sveltekit.md |
| systemd | https://bun.com/docs/guides/ecosystem/systemd.md |
| Vite | https://bun.com/docs/guides/ecosystem/vite.md |
| Upstash Redis | https://bun.com/docs/guides/ecosystem/upstash.md |

### HTTP / WebSocket / process

| Topic | URL |
|---|---|
| Common HTTP server | https://bun.com/docs/guides/http/server.md |
| Simple HTTP server | https://bun.com/docs/guides/http/simple.md |
| fetch request | https://bun.com/docs/guides/http/fetch.md |
| Hot reload server | https://bun.com/docs/guides/http/hot.md |
| Cluster / reusePort | https://bun.com/docs/guides/http/cluster.md |
| TLS on server | https://bun.com/docs/guides/http/tls.md |
| Proxy fetch | https://bun.com/docs/guides/http/proxy.md |
| Stream file as Response | https://bun.com/docs/guides/http/stream-file.md |
| FormData uploads | https://bun.com/docs/guides/http/file-uploads.md |
| fetch + unix socket | https://bun.com/docs/guides/http/fetch-unix.md |
| Streaming (async iterators) | https://bun.com/docs/guides/http/stream-iterator.md |
| SSE | https://bun.com/docs/guides/http/sse.md |
| Streaming (Node streams) | https://bun.com/docs/guides/http/stream-node-streams-in-bun.md |
| Simple WebSocket | https://bun.com/docs/guides/websocket/simple.md |
| Pub/sub WebSocket | https://bun.com/docs/guides/websocket/pubsub.md |
| WebSocket context | https://bun.com/docs/guides/websocket/context.md |
| WebSocket compression | https://bun.com/docs/guides/websocket/compression.md |
| Spawn | https://bun.com/docs/guides/process/spawn.md |
| Spawn stdout | https://bun.com/docs/guides/process/spawn-stdout.md |
| Spawn stderr | https://bun.com/docs/guides/process/spawn-stderr.md |
| argv | https://bun.com/docs/guides/process/argv.md |
| stdin | https://bun.com/docs/guides/process/stdin.md |
| IPC | https://bun.com/docs/guides/process/ipc.md |
| CTRL+C | https://bun.com/docs/guides/process/ctrl-c.md |
| OS signals | https://bun.com/docs/guides/process/os-signals.md |
| Nanoseconds uptime | https://bun.com/docs/guides/process/nanoseconds.md |

### Install

| Topic | URL |
|---|---|
| Add dependency | https://bun.com/docs/guides/install/add.md |
| Add devDependency | https://bun.com/docs/guides/install/add-dev.md |
| Add optional | https://bun.com/docs/guides/install/add-optional.md |
| Add peer | https://bun.com/docs/guides/install/add-peer.md |
| Git dependency | https://bun.com/docs/guides/install/add-git.md |
| Tarball dependency | https://bun.com/docs/guides/install/add-tarball.md |
| npm alias | https://bun.com/docs/guides/install/npm-alias.md |
| Workspaces | https://bun.com/docs/guides/install/workspaces.md |
| Custom registry | https://bun.com/docs/guides/install/custom-registry.md |
| Scope registry | https://bun.com/docs/guides/install/registry-scope.md |
| Azure Artifacts | https://bun.com/docs/guides/install/azure-artifacts.md |
| Artifactory | https://bun.com/docs/guides/install/jfrog-artifactory.md |
| Trusted dependency | https://bun.com/docs/guides/install/trusted.md |
| yarn.lock | https://bun.com/docs/guides/install/yarnlock.md |
| Migrate from npm | https://bun.com/docs/guides/install/from-npm-install-to-bun-install.md |
| Diff bun.lockb | https://bun.com/docs/guides/install/git-diff-bun-lockfile.md |
| CI install | https://bun.com/docs/guides/install/cicd.md |

### Test recipes

| Topic | URL |
|---|---|
| Run tests | https://bun.com/docs/guides/test/run-tests.md |
| Watch mode | https://bun.com/docs/guides/test/watch-mode.md |
| Jest → bun test | https://bun.com/docs/guides/test/migrate-from-jest.md |
| Mock functions | https://bun.com/docs/guides/test/mock-functions.md |
| Spy on | https://bun.com/docs/guides/test/spy-on.md |
| Mock clock | https://bun.com/docs/guides/test/mock-clock.md |
| Snapshots | https://bun.com/docs/guides/test/snapshot.md |
| Update snapshots | https://bun.com/docs/guides/test/update-snapshots.md |
| Coverage | https://bun.com/docs/guides/test/coverage.md |
| Coverage threshold | https://bun.com/docs/guides/test/coverage-threshold.md |
| Concurrent glob | https://bun.com/docs/guides/test/concurrent-test-glob.md |
| Skip | https://bun.com/docs/guides/test/skip-tests.md |
| Todo | https://bun.com/docs/guides/test/todo-tests.md |
| Timeout | https://bun.com/docs/guides/test/timeout.md |
| Bail | https://bun.com/docs/guides/test/bail.md |
| rerun-each | https://bun.com/docs/guides/test/rerun-each.md |
| Testing Library | https://bun.com/docs/guides/test/testing-library.md |
| happy-dom | https://bun.com/docs/guides/test/happy-dom.md |
| Svelte + bun test | https://bun.com/docs/guides/test/svelte-test.md |

### Read / write files

| Topic | URL |
|---|---|
| Read string | https://bun.com/docs/guides/read-file/string.md |
| Read Buffer | https://bun.com/docs/guides/read-file/buffer.md |
| Read Uint8Array | https://bun.com/docs/guides/read-file/uint8array.md |
| Read ArrayBuffer | https://bun.com/docs/guides/read-file/arraybuffer.md |
| Read JSON | https://bun.com/docs/guides/read-file/json.md |
| MIME type | https://bun.com/docs/guides/read-file/mime.md |
| Exists | https://bun.com/docs/guides/read-file/exists.md |
| Watch directory | https://bun.com/docs/guides/read-file/watch.md |
| Read stream | https://bun.com/docs/guides/read-file/stream.md |
| Write string | https://bun.com/docs/guides/write-file/basic.md |
| Write Blob | https://bun.com/docs/guides/write-file/blob.md |
| Write Response | https://bun.com/docs/guides/write-file/response.md |
| Append | https://bun.com/docs/guides/write-file/append.md |
| FileSink | https://bun.com/docs/guides/write-file/filesink.md |
| Write stream | https://bun.com/docs/guides/write-file/stream.md |
| Write stdout | https://bun.com/docs/guides/write-file/stdout.md |
| Cat to stdout | https://bun.com/docs/guides/write-file/cat.md |
| Copy file | https://bun.com/docs/guides/write-file/file-cp.md |
| Unlink | https://bun.com/docs/guides/write-file/unlink.md |

### HTMLRewriter / binary / streams

| Topic | URL |
|---|---|
| Extract links | https://bun.com/docs/guides/html-rewriter/extract-links.md |
| Extract OG tags | https://bun.com/docs/guides/html-rewriter/extract-social-meta.md |
| ArrayBuffer → string | https://bun.com/docs/guides/binary/arraybuffer-to-string.md |
| ArrayBuffer → Buffer | https://bun.com/docs/guides/binary/arraybuffer-to-buffer.md |
| ArrayBuffer → Blob | https://bun.com/docs/guides/binary/arraybuffer-to-blob.md |
| ArrayBuffer → number[] | https://bun.com/docs/guides/binary/arraybuffer-to-array.md |
| ArrayBuffer → Uint8Array | https://bun.com/docs/guides/binary/arraybuffer-to-typedarray.md |
| Buffer → string | https://bun.com/docs/guides/binary/buffer-to-string.md |
| Buffer → ArrayBuffer | https://bun.com/docs/guides/binary/buffer-to-arraybuffer.md |
| Buffer → Blob | https://bun.com/docs/guides/binary/buffer-to-blob.md |
| Buffer → Uint8Array | https://bun.com/docs/guides/binary/buffer-to-typedarray.md |
| Buffer → ReadableStream | https://bun.com/docs/guides/binary/buffer-to-readablestream.md |
| Blob → string | https://bun.com/docs/guides/binary/blob-to-string.md |
| Blob → ArrayBuffer | https://bun.com/docs/guides/binary/blob-to-arraybuffer.md |
| Blob → Uint8Array | https://bun.com/docs/guides/binary/blob-to-typedarray.md |
| Blob → DataView | https://bun.com/docs/guides/binary/blob-to-dataview.md |
| Blob → stream | https://bun.com/docs/guides/binary/blob-to-stream.md |
| Uint8Array → string | https://bun.com/docs/guides/binary/typedarray-to-string.md |
| Uint8Array → ArrayBuffer | https://bun.com/docs/guides/binary/typedarray-to-arraybuffer.md |
| Uint8Array → Buffer | https://bun.com/docs/guides/binary/typedarray-to-buffer.md |
| Uint8Array → Blob | https://bun.com/docs/guides/binary/typedarray-to-blob.md |
| Uint8Array → DataView | https://bun.com/docs/guides/binary/typedarray-to-dataview.md |
| Uint8Array → ReadableStream | https://bun.com/docs/guides/binary/typedarray-to-readablestream.md |
| DataView → string | https://bun.com/docs/guides/binary/dataview-to-string.md |
| ReadableStream → string | https://bun.com/docs/guides/streams/to-string.md |
| ReadableStream → JSON | https://bun.com/docs/guides/streams/to-json.md |
| ReadableStream → Blob | https://bun.com/docs/guides/streams/to-blob.md |
| ReadableStream → Buffer | https://bun.com/docs/guides/streams/to-buffer.md |
| ReadableStream → ArrayBuffer | https://bun.com/docs/guides/streams/to-arraybuffer.md |
| ReadableStream → Uint8Array | https://bun.com/docs/guides/streams/to-typedarray.md |
| ReadableStream → chunks | https://bun.com/docs/guides/streams/to-array.md |
| Node Readable → string | https://bun.com/docs/guides/streams/node-readable-to-string.md |
| Node Readable → JSON | https://bun.com/docs/guides/streams/node-readable-to-json.md |
| Node Readable → Blob | https://bun.com/docs/guides/streams/node-readable-to-blob.md |
| Node Readable → Uint8Array | https://bun.com/docs/guides/streams/node-readable-to-uint8array.md |
| Node Readable → ArrayBuffer | https://bun.com/docs/guides/streams/node-readable-to-arraybuffer.md |

## Changelog

`https://bun.com/blog/bun-v<version>` — latest `1.4.2` (2026-09-05):
https://bun.com/blog/bun-v1.4.2

Fetch the `.md` twin when it exists. Bun 1.4.1 and 1.4.2 have one; fall back
to the HTML post for releases such as 1.4.0 whose twin is missing. The 1.4.1
and 1.4.2 posts have an upgrade command but no Upgrading/breaking section.

| Release | Topic | URL |
|---|---|---|
| 1.4.2 | Release post (latest) | https://bun.com/blog/bun-v1.4.2 |
| 1.4.2 | Upgrade command | https://bun.com/blog/bun-v1.4.2#to-upgrade-bun |
| 1.4.2 | `bun build` variable-name regression | https://bun.com/blog/bun-v1.4.2#fixed-bun-build-variable-name-collision |
| 1.4.2 | `AsyncLocalStorage` memory leak | https://bun.com/blog/bun-v1.4.2#fixed-asynclocalstorage-memory-leak |
| 1.4.2 | `worker_threads` `online` event order | https://bun.com/blog/bun-v1.4.2#fixed-worker-threads-online-event-order |
| 1.4.2 | `Bun.Image` CMYK/YCCK JPEG decoding | https://bun.com/blog/bun-v1.4.2#fixed-bun-image-decodes-cmyk-and-ycck-jpegs |
| 1.4.1 | Release post | https://bun.com/blog/bun-v1.4.1 |
| 1.4.1 | Upgrade command | https://bun.com/blog/bun-v1.4.1#to-upgrade-bun |
| 1.4.1 | `Bun.serve` HTTP/2 (experimental) | https://bun.com/blog/bun-v1.4.1#bun-serve-supports-http-2 |
| 1.4.1 | Streaming `Bun.write(path, Response)` | https://bun.com/blog/bun-v1.4.1#bun-write-path-response-streams-to-disk |
| 1.4.1 | WebSocket `pause()` / `resume()` | https://bun.com/blog/bun-v1.4.1#websocket-supports-pause-and-resume |
| 1.4.1 | `crypto.argon2` / `argon2Sync` | https://bun.com/blog/bun-v1.4.1#node-crypto-supports-crypto-argon2-and-crypto-argon2sync |
| 1.4.1 | `--env-file` pipes, FIFOs, stdin | https://bun.com/blog/bun-v1.4.1#env-file-reads-pipes-fifos-and-dev-stdin |
| 1.4.1 | `--no-ffi-cc` | https://bun.com/blog/bun-v1.4.1#no-ffi-cc-disables-cc-from-bun-ffi |
| 1.4.1 | Self-contained workspace `node_modules` | https://bun.com/blog/bun-v1.4.1#self-contained-node-modules-for-workspace-packages |
| 1.4.1 | `bun install --offline` | https://bun.com/blog/bun-v1.4.1#bun-install-offline |
| 1.4.1 | `bun install --prefer-offline` | https://bun.com/blog/bun-v1.4.1#bun-install-prefer-offline |
| 1.4.1 | `--min-chunk-size` / `minChunkSize` | https://bun.com/blog/bun-v1.4.1#min-chunk-size |
| 1.4.1 | `--bytecode-depth` | https://bun.com/blog/bun-v1.4.1#smaller-bytecode |
| 1.4.1 | Cross-compile with `--bytecode` | https://bun.com/blog/bun-v1.4.1#cross-compile-with-bytecode |
| 1.4.1 | `fetch()` TLS hostname behavior change | https://bun.com/blog/bun-v1.4.1#fetch-verifies-tls-against-the-url-not-the-host-header |
| 1.4.0 | Upgrading / breaking changes | https://bun.com/blog/bun-v1.4.0#upgrading-to-1-4 |
| 1.4.0 | `--cpu-prof` / `--heap-prof` | https://bun.com/blog/bun-v1.4.0#dev-tooling |
| 1.4.0 | `process.on("memoryPressure")` | https://bun.com/blog/bun-v1.4.0#process-on-memorypressure |
| 1.4.0 | HTTP/2 and HTTP/3 `fetch` (experimental) | https://bun.com/blog/bun-v1.4.0#http-2-http-3-in-fetch-experimental |
| 1.4.0 | React Compiler | https://bun.com/blog/bun-v1.4.0#built-in-react-compiler |
| 1.4.0 | Per-PR notes | https://bun.com/blog/release-notes/bun-v1.4.0 |
| — | Rust rewrite | https://bun.com/blog/bun-in-rust |
| — | Node.js test suite tracker | https://bun.com/node-test-suite |
| — | Blog index | https://bun.com/blog |
