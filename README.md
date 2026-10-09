# Ullas Opskrifter MCP

<img src="assets/icon-512.png" width="96" alt="Ullas Opskrifter icon">

Read-only [Model Context Protocol](https://modelcontextprotocol.io) server for the Danish recipe collection at [ullasopskrifter.dk](https://ullasopskrifter.dk).

- **Endpoint:** `https://ullasopskrifter.dk/mcp` (Streamable HTTP)
- **Auth:** none. All tools are read-only and return only published recipes.
- **Registry name:** `dk.ullasopskrifter/recipes`
- **Support:** agent@mitc.dk

This repository holds only documentation and registry metadata (`server.json`, icon). It contains no site code and no recipe data.

## Tools

| Tool | What it does |
|---|---|
| `search_recipes` | Full-text search across recipe titles, ingredients and instructions (`q`). |
| `recipes_list` | List published recipes with pagination (`page`, `limit` up to 100). |
| `recipes_get` | Get one recipe by numeric id or slug (`id_or_slug`): ingredients, method, categories, image and page URL. |
| `ingredients_search_recipes` | Find recipes whose ingredient list contains the given text (`ingredient`). |
| `categories_list` | List recipe categories as a tree with recipe counts. |
| `categories_recipes` | List recipes in a category including child categories (`slug`, optional `sort`: title, newest, views, views30). |

Schemas: see [docs/tools.md](docs/tools.md).

## Connect

Claude Code:

```bash
claude mcp add --transport http ullas https://ullasopskrifter.dk/mcp
```

Cursor / VS Code style `mcp.json`:

```json
{ "mcpServers": { "ullas": { "url": "https://ullasopskrifter.dk/mcp" } } }
```

Other clients (Claude, ChatGPT developer mode, Grok, Perplexity, Mistral): add a custom connector with the URL above and no authentication.

## Example prompts

- "Find a Danish recipe with rødspætte."
- "List the recipe categories."
- "Which recipes contain kartofler?"

## Content and licence

The MIT licence in this repository covers the documentation and metadata only. Recipes and images are the property of ullasopskrifter.dk and are provided for personal, non-commercial use.

## Contact

agent@mitc.dk, operated by MITC.
