# Installing the AppClap MCP server

AppClap is a hosted, remote MCP server. There is nothing to download, build
or run locally, and no API key is needed.

1. Add a remote MCP server named `appclap` with this URL (Streamable HTTP):
   `https://mcp.app-clap.com/mcp`
2. No headers, environment variables or arguments are required.
3. Confirm it works by calling `search_apps` with
   `{"need": "a free form builder"}` — it returns a ranked list of web apps.

Optional: a free key (sign in at https://app-clap.com → account → MCP) or the
sign-in address `https://mcp.app-clap.com/mcp/signin` adds live web research
when the catalog has nothing, and lifts the shared daily limit for calls
without a key.
