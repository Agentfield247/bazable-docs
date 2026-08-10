
#### `docs/commands/login.md`
```markdown
# bazable login / logout

Stores or removes API credentials and cloud authentication tokens.

## Usage
```bash
bazable login [options]
bazable logout

Options (login)
-e, --email <email> : Your login email

-p, --password <password> : Your login password

-t, --token <token> : A pre‑obtained access token

-b, --base-url <url> : Base URL of the API

--supabase-url <url> : Supabase project URL

--supabase-key <key> : Supabase anon key

## Examples
bazable login -e admin@example.com -p secret123
bazable logout
