# bazable extract (ext, e)

Scans your codebase for API calls and adds any undocumented endpoints to the contract.

## Usage
bazable extract [options]

## Options
- -r, --payloads : Also infer request payload schemas
- -s, --preset <name> : Use a pre‑configured pattern (py, php, go, rb, js, ax)
- --pattern <regex> : Custom regex for URL extraction
- --ext <extensions...> : File extensions to scan (e.g. .py .rb)
- --ignore <patterns...> : Glob patterns to ignore (e.g. venv dist)
- --wrapper <names...> : Custom API wrapper function names

## Examples

Standard extraction with payload inference:
bazable extract -r

Python project:
bazable extract -s py

Custom regex:
bazable extract --pattern 'requests\.get\("([^"]+)"' --ext .py
