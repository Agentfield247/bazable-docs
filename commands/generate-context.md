# bazable gen context

Generates AI agent context files in your project root so that AI coding tools (Cursor, Cline, Roo Code) automatically respect your Bazable contract.

## Usage

```bash
bazable gen context
```

## Options

- `-o, --output <dir>` : Output directory for the generated files (default is the current working directory)

## What it creates

| File | Purpose |
|------|---------|
| `.cursorrules` | Instructions for **Cursor IDE**. Cursor reads this file and follows the rules when suggesting or writing code. |
| `.clinerules` | Instructions for **Cline / Roo Code / VS Code** agents. These tools use the rules to avoid hallucinating API calls. |
| `.mcp.json` | Pre‑configures **Bazable’s MCP server** as an active tool. MCP‑compatible agents (like Cursor with MCP) can then call `bazable.inspect`, `bazable.listEndpoints`, etc. directly. |

## What to do after generation

1. **Restart your AI coding tool** (Cursor, Cline, etc.) – it will automatically detect the new context files.
2. **Start the MCP server** in your project directory if you want real‑time contract data:
   ```bash
   bazable mcp
   ```
3. The AI agent will now:
   - Check `bazable.config.json` instead of inventing API endpoints.
   - Use your generated `bazableClient` or `bazable-types` for type‑safe API calls.
   - Verify contract compliance before proposing changes.

## Example

```bash
bazable gen context
```

After running, you’ll see:

```
✦ Generated .cursorrules
✦ Generated .clinerules
✦ Generated .mcp.json
```
