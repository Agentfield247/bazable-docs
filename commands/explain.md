```markdown
# bazable explain

Uses AI to provide a plain‑English explanation of an endpoint.

## Usage
```bash
bazable explain <method> <url>
```

## Options
None.

## Prerequisites
- An AI API key must be configured. Run `bazable config --set-ai-key <your-key>` (and optionally `--set-ai-base` and `--set-ai-model` if you’re using a provider other than OpenAI).  
- The endpoint must exist in your `bazable.config.json` with a request and/or response schema.

## What it does
The command sends the endpoint’s method, URL, request schema, and response schema to the configured AI model. The AI returns a concise, plain‑English summary covering:

- What the endpoint does
- What data must be sent
- What data will be returned
- Any edge cases or common pitfalls

The explanation is printed directly in the terminal.

## Example
```bash
bazable explain POST https://api.example.com/v1/users
```

Example output:

```
--- Explanation for POST https://api.example.com/v1/users ---
This endpoint creates a new user. You must send a JSON body with `name` (string) and `email` (string). On success, it returns the created user object with an `id`, `name`, and `email`. Make sure the email is unique – the API may return an error if a duplicate is detected.
```
```
