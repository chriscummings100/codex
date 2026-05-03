---
name: shopme
description: Use ShopMe when the user wants help with grocery shopping, grocery lists, meal-to-shopping planning, grocery item lookup, or cart-style grocery workflows through the bundled ShopMe MCP server.
---

# ShopMe

Use this skill when a user asks Codex to help with grocery shopping, grocery list organization, meal-to-shopping planning, pantry-aware shopping, item lookup, or any workflow that should use the ShopMe grocery MCP tools.

## MCP Server

This plugin provides the `shopme` MCP server. It is launched from npm with:

```bash
npx -y @chriscummings100/shopme-mcp-groceries
```

When the ShopMe MCP tools are available, prefer those tools over manually inventing grocery data. Inspect the available tool names and schemas, then choose the narrowest tool that matches the user's request.

## Workflow

1. Clarify the user's shopping goal only when required information is missing, such as store, dietary restrictions, budget, household size, or whether substitutions are acceptable.
2. Use the ShopMe MCP tools for grocery-specific data, list operations, search, or cart-like actions.
3. Keep quantities, units, and substitutions explicit so the resulting shopping list is easy to act on.
4. Before any irreversible or purchase-like action, summarize the intended change and get explicit confirmation from the user.

## Response Style

Return concise grocery plans or shopping lists grouped by practical store sections when that helps the user shop. Include assumptions briefly, especially for substitutions, quantities, prices, or unavailable details.
