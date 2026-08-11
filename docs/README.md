# TestLab documentation

Mintlify product docs for TestLab (web app, CLI/SDK, CI, and API reference).

## Local preview

```bash
npm install -g mintlify
mintlify dev
```

Open the printed local URL (often `http://localhost:3000`).

## Layout

- `mint.json` — site name, tabs, navigation
- `index.mdx` — product home
- `docs/introduction.mdx`, `docs/authentication.mdx`
- `docs/concepts/` — domain language
- `docs/web-app/` — UI guides + screenshots
- `docs/cli-sdk/` — CLI login/init, Playwright, Client
- `docs/ci-automations/` — CI reporting + Automations
- `docs/guides/` — recipes
- `docs/api-reference/` + `docs/openapi.yaml` — API reference
- `images/screenshots/` — UI captures (redacted)

## Source of product truth

Feature inventory and coverage notes may also live temporarily in
`poc-test-management/research/docs-completeness/`. Authored pages ship here.
