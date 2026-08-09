# bazable mcp

Starts a **Model Context Protocol (MCP) server** that allows AI coding agents (Cursor, Claude Code, Copilot, etc.) to interact with Bazable natively.

Once started, the server listens on `stdin`/`stdout` for JSON‑RPC requests and exposes real, production‑ready tools that inspect your contract and run tests.

---

## Available tools

| Tool | Description | Input |
|------|-------------|-------|
| `listEndpoints` | Returns all contracted endpoints with their HTTP methods and statuses. | *(none)* |
| `getEndpoint` | Returns the request and response schemas for a specific endpoint. | `method` (string), `url` (string) |
| `inspect` | Runs a full contract inspection (`bazable inspect --json --ci`) and returns violations as JSON. | *(none)* |
| `test` | Runs mock tests on all endpoints (`bazable test --json --mock --all`) and returns pass/fail results. | *(none)* |

---

## Usage

```bash
bazable mcp
