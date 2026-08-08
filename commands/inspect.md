# bazable inspect (i, check)

Validates your code against the contract. Detects dead URLs, payload type mismatches, and over‑fetching.

## Usage
bazable inspect [options]

## Options
- -f, --fix : Auto‑correct simple type mismatches in source files
- All extraction options (presets, patterns, extensions, etc.)

## Examples

Check for violations:
bazable inspect

Auto‑fix payload mismatches:
bazable inspect -f
