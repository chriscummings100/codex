# ShopMe Codex Plugin

This repository packages the ShopMe grocery MCP server and its companion Codex skill as a Codex plugin.

## Contents

- `plugins/shopme/.codex-plugin/plugin.json` is the plugin manifest.
- `plugins/shopme/.mcp.json` launches the ShopMe MCP server with `npx -y @chriscummings100/shopme-mcp-groceries`.
- `plugins/shopme/skills/shopme/SKILL.md` tells Codex when and how to use ShopMe.
- `.agents/plugins/marketplace.json` provides a local marketplace entry that points at `./plugins/shopme`.

## Local Testing

Clone this repository, then use the marketplace entry at `.agents/plugins/marketplace.json` to install or test the local `shopme` plugin in Codex.

The MCP server is resolved from npm at install or use time, so Node.js and `npx` must be available in the environment where Codex launches MCP servers.

From this repository root, add the local marketplace with:

```bash
codex plugin marketplace add .
```

After publishing to GitHub, add the marketplace directly from the repository:

```bash
codex plugin marketplace add chriscummings100/shopme
```

You can pin a branch, tag, or commit with:

```bash
codex plugin marketplace add chriscummings100/shopme@main
```

To update an already-added marketplace, run:

```bash
codex plugin marketplace upgrade shopme
```

## Before Publishing

Replace the remaining `[TODO: ...]` fields in `plugins/shopme/.codex-plugin/plugin.json`, especially contact email, license, privacy policy, and terms of service. Update the homepage and repository URLs if the GitHub repository uses a different name.
