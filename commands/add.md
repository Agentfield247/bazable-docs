# bazable add

Fetches a live API endpoint and stores its response schema in the contract.

## Usage
```bash
bazable add <url> [options]

Options
-m, --method <method> : HTTP method (default GET)

-t, --token <token> : Access token for authenticated endpoints

-H, --header <headers...> : Additional headers (key:value)

## Example

bazable add https://jsonplaceholder.typicode.com/posts/1
bazable add https://api.example.com/v1/users --method POST --token "your-token"
