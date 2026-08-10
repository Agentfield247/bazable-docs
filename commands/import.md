
#### `docs/commands/import.md`
```markdown
# bazable import (imp)

Imports API specifications (OpenAPI v2/v3, Postman collections, CSV) and merges endpoints into the contract.

## Usage
```bash
bazable import [source] [options]

Options
-b, --base-url <url> : Base URL to resolve relative paths

--csv <filePath> : Import from a CSV file

--name <endpointName> : Endpoint name when importing CSV

## Example
bazable import openapi.yaml
bazable import https://api.example.com/swagger.json
bazable import --csv products.csv --name products
