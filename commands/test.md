# bazable test

Sends real HTTP requests to every contracted endpoint and reports health.

## Usage
bazable test [options]

## Options
- -t, --token <token> : Access token
- -e, --email <email> : Auto‑login email
- -p, --password <password> : Auto‑login password
- -m, --method <method> : HTTP method (default GET)
- -w, --write : Allow testing of write endpoints
- -k, --mock : Mock mode (no real requests)
- -a, --all : Test all endpoints regardless of status
- -x, --exclude <urls...> : Skip specific endpoints

## Examples

Mock‑test all endpoints:
bazable test -k -a

Real test with auto‑login:
bazable test -e admin@example.com -p secret123 -m POST -w
