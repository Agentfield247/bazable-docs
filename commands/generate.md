# bazable generate (gen)

Generates backend code from the contract.

## Subcommands
- backend : Express.js or Hono router stubs with validation

## Usage
bazable gen backend [options]

## Options
- -f, --framework <name> : express or hono
- -o, --output <dir> : Output directory
- -v, --no-validation : Skip Zod validation schemas

## Example
bazable gen backend -f express -o ./api
