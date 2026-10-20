# AppClap MCP server

Find the web app that fits a need — ranked by fit alone, never by popularity
or payment — with facts read from each vendor's own site and the date they
were last checked.

[AppClap](https://app-clap.com) is a catalog of 8,600+ web apps, including
the small and brand-new ones web search and model training data miss. This
server lets any AI assistant or agent query it over the
[Model Context Protocol](https://modelcontextprotocol.io).

- **Endpoint:** `https://mcp.app-clap.com/mcp` (Streamable HTTP, hosted)
- **Access:** free, no key needed
- **Docs:** https://app-clap.com/mcp.md
- **Registry:** `com.app-clap/appclap` in the
  [official MCP Registry](https://registry.modelcontextprotocol.io)

This repository holds the connection details and listing files only. The
server itself is hosted by AppClap; there is nothing to install or run.

## Why not just ask your AI or Google?

1. **Finds apps beyond the famous names.** AI and Google keep suggesting the
   same big tools. AppClap also covers small and brand-new apps that rarely
   show up in either, and they're often cheaper.
2. **Up-to-date prices and features.** AI answers from what it learned months
   ago. AppClap reads every fact from the app's own website and shows the date
   it was checked.
3. **No made-up facts.** When a price or feature isn't published, AppClap says
   "not stated" instead of guessing.
4. **Filter by what matters to you:** free plan, a price limit, open source,
   self-hosted, or "an alternative to X". Just say it in your request.
5. **Compare in one step, not ten tabs.** Pricing, free plan, trial and
   features side by side, in each app's own currency.
6. **Ranked by fit, never by money.** No ads, no paid placement, no sponsored
   lists.

Free, no key needed.

## Tools

| Tool | What it does |
|---|---|
| `search_apps` | Ranked web apps for a plain-language need ("a free form builder", "an open-source alternative to Notion", "a CRM under $20/month"). |
| `get_app` | The full record for one app: pricing in the vendor's own currency and plans, features, platforms, open-source and self-hosting status. |
| `compare_apps` | Two to five apps side by side: pricing, free tier, trial, open source, shared and distinct features. |
| `submit_app` | Add a web app to the catalog. Everything is verified against the app's own site before it appears. |
| `report_app_issue` | Flag a wrong or outdated detail on a listed app; it triggers a re-check against the site. |

Every fact comes from the vendor's own site. A missing fact is reported as
"not stated", never guessed. Nobody pays for position.

## Connect

**Claude** (claude.ai or Desktop): Settings → Connectors → Add custom
connector → `https://mcp.app-clap.com/mcp/signin` (sign in once, free), or
`https://mcp.app-clap.com/mcp` to use it without signing in.

**Claude Code**

```bash
claude mcp add --transport http appclap https://mcp.app-clap.com/mcp
```

**Cursor** (`~/.cursor/mcp.json`)

```json
{
  "mcpServers": {
    "appclap": { "url": "https://mcp.app-clap.com/mcp" }
  }
}
```

**VS Code** (`.vscode/mcp.json`)

```json
{
  "servers": {
    "appclap": { "type": "http", "url": "https://mcp.app-clap.com/mcp" }
  }
}
```

**Gemini CLI**

```bash
gemini extensions install https://github.com/AppClap-Org/appclap-mcp
```

**Any other client:** add a remote (Streamable HTTP) MCP server with the URL
`https://mcp.app-clap.com/mcp`.

## Signing in (optional)

Without a key, `search_apps`, `get_app` and `compare_apps` work straight away
within a daily limit shared by everyone calling without a key. Signing in is
free and adds live web research when the catalog has nothing, and lifts that
shared limit. Get a key at https://app-clap.com (account → MCP), or connect
through `https://mcp.app-clap.com/mcp/signin`.

## Contact

hello@app-clap.com · [Privacy](https://app-clap.com/privacy) ·
[Terms](https://app-clap.com/terms)
