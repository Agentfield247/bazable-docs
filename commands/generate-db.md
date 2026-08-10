
#### `docs/commands/generate-db.md`
```markdown
# bazable gen db

Generates database schema (Prisma model or Supabase SQL migration) from an endpoint's request/response schemas.

## Usage
```bash
bazable gen db <method> <url> [options]

Options
-o, --output <dir> : Output directory (default ./generated-db)

--orm <type> : ORM framework (prisma or supabase, default prisma)

## Example 
bazable gen db POST https://api.example.com/v1/settlements --orm prisma
