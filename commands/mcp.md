# bazable mcp

Starts a **Model Context Protocol (MCP) server** that allows AI coding agents (Cursor, Claude Code, Copilot, etc.) to interact with Bazable natively.

Once started, the server listens on `stdin`/`stdout` for JSON‑RPC requests and exposes the following tools:

- `listEndpoints` – returns all contracted endpoints with their HTTP methods and statuses
- `getEndpoint` – accepts `method` and `url`, returns the request and response schemas for that endpoint
- `inspect` – runs a full contract inspection (`bazable inspect --json --ci`) and returns violations as JSON
- `test` – runs mock tests on all endpoints (`bazable test --json --mock --all`) and returns pass/fail results

## Usage
```bash
bazable mcp
