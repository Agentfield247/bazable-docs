
#### `docs/commands/types.md`
```markdown
# bazable types

Generates TypeScript interfaces from the stored response schemas.

## Usage
```bash
bazable types [options]

Options
-o, --output <dir> : Output directory (default current directory)

--stdout : Print to terminal instead of writing a file

--prefix <prefix> : Prefix for interface names

--name <name> : Override interface name (only for a single schema)

## Example
bazable types -o ./src/types
