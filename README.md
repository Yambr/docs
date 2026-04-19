# Yambr docs

Source for [docs.yambr.com](https://docs.yambr.com/) — documentation for [Open Computer Use](https://github.com/Yambr/open-computer-use) as deployed on the Yambr platform (`api.yambr.com`, `app.yambr.com`, `chat.yambr.com`, `cu.yambr.com`).

Built with [Mintlify](https://mintlify.com/).

## Local preview

```bash
npm i -g mint
mint dev
```

Open http://localhost:3000. Edits to `.mdx` files hot-reload.

## Layout

```
/
├── docs.json             # Navigation, branding, anchors
├── index.mdx             # Landing
├── quickstart.mdx
├── introduction.mdx
├── architecture.mdx
├── platform/             # Yambr-specific services (api, app, chat, cu)
├── install/              # Self-hosting
├── features/             # Browser, terminal, code exec, sub-agents, file preview
├── skills/               # Skills system
├── integrations/         # Open WebUI, Claude Desktop, LiteLLM, n8n, custom
├── reference/            # Comparison, system prompt, known bugs, changelog, contributing
├── api-reference/        # MCP methods
├── images/
│   ├── diagrams/         # SVGs from the upstream repo
│   ├── screenshots/      # Product screenshots
│   └── openwebui-hero.png
└── logo/
    └── yambr.png
```

## Content source

Most of the technical content was ported from [github.com/Yambr/open-computer-use/tree/main/docs](https://github.com/Yambr/open-computer-use/tree/main/docs). When the upstream .md changes, mirror the update into the matching `.mdx` here.

## Deploy

Pushes to `main` are picked up by the Mintlify GitHub App and shipped to [docs.yambr.com](https://docs.yambr.com/) automatically.

## Editing tips

- Link between docs with clean `/route` paths — e.g. `/platform/api-keys`, `/api-reference/mcp/initialize`.
- Images live under `/images/...`; reference them absolute (`<img src="/images/diagrams/architecture.svg" />`).
- Components available: `<Card>`, `<CardGroup>`, `<Steps>`, `<Step>`, `<Frame>`, `<Note>`, `<Warning>`, `<Tip>`, `<CodeGroup>`, `<AccordionGroup>`, `<Accordion>`.
- When referring to the four Yambr services, prefer the domain form (`api.yambr.com`, `chat.yambr.com`, ...) — not "the API" / "the chat" — so readers can always grep for the right thing.

## Contributing

Small fixes: PR directly. Bigger rewrites: open an issue first. Canonical reference is still the upstream repo's `README.md`, `CHANGELOG.md`, and files under `docs/` — keep this site in sync.
