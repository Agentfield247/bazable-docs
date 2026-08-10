
#### `docs/commands/diff.md`
```markdown
# bazable diff

Compares the stored contract schema against the live API and highlights breaking changes.

## Usage
```bash
bazable diff [url] [options]

Options
-t, --token <token> : Access token

-m, --method <method> : HTTP method (default GET)

--base-url <url> : Override base URL

--base-path <path> : Explicit path to append to base URL

--breaking-only : Show only breaking changes

--json : Output diff as JSON

--accept : Automatically update contract to match live API

## Example
bazable diff
bazable diff https://api.example.com/v1/users --json
bazable diff --accept
