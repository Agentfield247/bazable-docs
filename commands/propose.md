# bazable propose

Submits a plain‑English request to the AI and generates a schema change proposal.

## Usage
bazable propose <request>

## Prerequisites
n AI API key must be configured. Run bazable config --set-ai-key <your-key> (and optionally --set-ai-base and --set-ai-model if you’re using a provider other than OpenAI).

Your bazable.config.json must contain at least one endpoint so the AI can understand the existing contract.

## What it does
Sends your plain‑English request (e.g. "Add a phone_number field to the POST /v1/users endpoint") to the AI along with the entire current contract.

The AI returns a JSON diff describing the exact schema changes needed (new fields, type changes, etc.).

The proposed change is displayed in the terminal in yellow.

You are then asked:
```text
Send this proposal to the backend team? (Y/n)

If you answer Y, the proposal is saved to the pending_proposals array in bazable.config.json. It can later be accepted with bazable accept <proposal-id>.

If you answer n, the proposal is discarded.


## Example
bazable propose "Add a phone number field to the POST /v1/users endpoint"

## Example Output
Proposed schema change:
{
  "endpoint": "POST https://api.example.com/v1/users",
  "changes": {
    "request": {
      "phone_number": "string"
    },
    "response": {
      "phone_number": "string"
    }
  }
}

Send this proposal to the backend team? (Y/n)
