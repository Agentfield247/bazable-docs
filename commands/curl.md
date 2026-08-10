# bazable curl

Sends a raw HTTP request from the terminal.  
Works exactly like `curl`, but with built‑in logging, error handling, and no CORS restrictions.

## Usage

```bash
bazable curl <url> [options]

Options
-X, --method <method> : HTTP method (default GET)

-H, --header <headers...> : Request headers (key:value)

-d, --data <body> : Request body (JSON string or plain text)

# Simple GET request
bazable curl https://jsonplaceholder.typicode.com/posts/1

# POST with headers and JSON body
bazable curl https://api.example.com/v1/users \
  -X POST \
  -H "Authorization: Bearer YOUR_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"name":"Alice","email":"alice@example.com"}'
