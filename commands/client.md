
#### `docs/commands/client.md`
```markdown
# bazable client

Generates a strictly‑typed API client (`bazableClient.ts`) with async functions for each contracted endpoint.

## Usage
```bash
bazable client [options]

Options
-o, --output <dir> : Output directory (default current directory)

--stdout : Print to terminal instead of writing a file

--prefix <prefix> : Prefix for function names

## Example
bazable client -o ./src/api
