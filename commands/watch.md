
#### `docs/commands/watch.md`
```markdown
# bazable watch

Continuously polls a remote contract (or cloud project) and auto‑fixes your code on changes.

## Usage
```bash
bazable watch [url] [options]

Options
-i, --interval <seconds> : Polling interval (default 60)

--dry-run : Show changes without applying them

--auto-accept : Automatically apply all changes

## Examples
bazable watch https://api.example.com/contract.json
bazable watch   # uses cloud project if linked
