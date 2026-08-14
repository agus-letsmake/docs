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
- `introduction.mdx`, `authentication.mdx`
- `concepts/` — domain language
- `web-app/` — UI guides + screenshots
- `cli-sdk/` — CLI login/init, Playwright, Client
- `ci-automations/` — CI reporting + Automations
- `guides/` — recipes
- `api-reference/` + `openapi.yaml` — API reference
- `images/screenshots/` — UI captures (redacted)

Hosted docs are proxied at `https://make-testlab.vercel.app/docs/...`
(for example `/docs/guides/quickstart`). Keep page files at the repo root so
Mintlify does not emit `/docs/docs/...`.

## Source of product truth

Feature inventory and coverage notes may also live temporarily in
`poc-test-management/research/docs-completeness/`. Authored pages ship here.
