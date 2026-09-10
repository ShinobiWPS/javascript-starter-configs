# Global OpenCode Preferences

When inspecting files, always use the read tool.
Do not use bash commands such as cat, grep, head, tail, or find unless strictly necessary.

## Runtime and package manager

Prefer `pnpm` for JavaScript and TypeScript projects unless the repository clearly uses another package manager.

Before suggesting large changes, inspect the project conventions first.

## Code style

Prefer TypeScript, explicit types at boundaries, and simple readable abstractions.

Use single quotes.

Avoid semicolons unless the project already requires them.

Prefer trailing commas in multiline structures.

Prefer tabs when the project is already configured that way; otherwise preserve the existing indentation style.

Prefer Biome when the project has Biome config.

Prefer ESLint when the project has ESLint config.

Prefer Prettier when the project has Prettier config.

Do not fight the repository formatter.

## Frontend defaults

For data fetching, prefer TanStack Query patterns when already present.

For forms, preserve the project’s chosen form library.

For styling, preserve the project’s chosen styling system.

## Git behavior

Never force-push without explicit approval.

Never run destructive git commands without explicit approval.

Before proposing a commit message, inspect the staged diff.

Commit messages should use conventional commit format:

`type(scope): description`

Use imperative mood.

Keep the subject concise.

Allowed types: feat, fix, docs, style, refactor, perf, test, chore, ci.

## Generated and sensitive files

Avoid editing generated files unless explicitly requested.

Treat these as generated or protected:

- `routeTree.gen.ts`
- `pnpm-lock.yaml`
- `bun.lock`
- `yarn.lock`
- `package-lock.json`
- `.env`
- `.env.*`
- `credentials.json`
- `credentials.*.json`
- `secret.json`
- `secrets.json`
- `*.key`
- `*.pem`
- `*.pfx`
- `*.p12`
- `*.crt`
- `*.cer`
- `id_rsa`
- `.ssh/id_*`

Do not print secrets, tokens, private keys, or credential file contents.

## Verification

When changing code, prefer these checks by default:

1. Typecheck
2. Lint

Run unit tests, integration/e2e tests, or builds only when the user explicitly requests them for the current task. A repository script or completion checklist does not count as an explicit request.

Explain failures with the exact command that failed and the smallest next action.

## Chrome MCP fallback

- Prefer `chrome-mcp-attach_*` tools first when using Chrome DevTools MCP.
- If any `chrome-mcp-attach_*` call fails, immediately retry the equivalent action with `chrome-mcp-new_*`.
- Only consider MCP unavailable after both attach and new variants fail.
