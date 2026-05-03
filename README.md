# Codex and Claude plugins

This repository is a plugin marketplace for Codex and Claude Code. It currently
publishes one plugin.

## Plugins

| Plugin | Version | Category | Description |
| --- | --- | --- | --- |
| `shopme` | `0.1.0` | Productivity | Grocery planning and shopping assistance through the ShopMe MCP server and companion skill. |

`shopme` configures the `shopme` MCP server with:

```json
{
  "command": "npx",
  "args": ["-y", "@chriscummings100/shopme-mcp-groceries"]
}
```

## Marketplace Layout

The repository contains both marketplace formats:

- Codex marketplace: `.agents/plugins/marketplace.json`
- Claude Code marketplace: `.claude-plugin/marketplace.json`

Each plugin can also include tool-specific manifests:

- Codex plugin manifest: `plugins/<plugin>/.codex-plugin/plugin.json`
- Claude Code plugin manifest: `plugins/<plugin>/.claude-plugin/plugin.json`
- MCP server config: `plugins/<plugin>/.mcp.json`
- Skills: `plugins/<plugin>/skills/`

## Install for Codex

Add the marketplace from GitHub:

```powershell
codex plugin marketplace add https://github.com/chriscummings100/codex.git
```

After adding the marketplace, restart or reopen Codex if the plugin list was
already loaded. `shopme` will appear as an available plugin from the `shopme`
marketplace.

Update the marketplace later with:

```powershell
codex plugin marketplace upgrade shopme
```

## Install for Claude Code

Add the marketplace from GitHub for your user account:

```powershell
claude plugin marketplace add https://github.com/chriscummings100/codex.git
```

Install the plugin after the marketplace is added:

```powershell
claude plugin install shopme
```
