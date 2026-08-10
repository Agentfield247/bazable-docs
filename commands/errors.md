
#### `docs/commands/errors.md`
```markdown
# bazable errors

Views or clears the persistent error log (`~/.bazable/errors.log`).

## Usage
```bash
bazable errors [options]

Options
-c, --clear : Clear the error log

-n, --lines <number> : Number of recent errors to show (default 20)

## Example
bazable errors
bazable errors -c
