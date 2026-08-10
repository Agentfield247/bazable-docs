# bazable ui

Opens a local web dashboard showing all endpoints, their schemas, and testing tools.

## Usage
bazable ui [options]

## What it provides
Endpoints table – view every endpoint in your contract, with HTTP method badges, status indicators, and quick‑action buttons (Send, Edit, Explain, Propose, Copy Cmd).

Stats cards – see at a glance how many endpoints are working, failed, or unverified.

API Tester – a built‑in, Postman‑style tool that lets you send raw HTTP requests to any URL, with custom headers and body. The dashboard’s server‑side proxy bypasses CORS restrictions.

Edit/Add/Delete endpoints – modify schemas directly from the browser without touching the JSON file.

AI Explain & Propose – click a button to get an AI‑generated plain‑English explanation of an endpoint, or submit a natural‑language request for a schema change.

Settings – update the base URL, configure your AI key (with a test‑connection button), and manage your webhook URL.

Login modal – save your API credentials so the dashboard can auto‑authenticate subsequent requests.

Dark/light mode toggle – persists your preference across sessions.

Refresh button – reloads the latest contract data without restarting the server.

## Prerequisites
Your project must contain a valid bazable.config.json with at least one endpoint.


## Options
- -p, --port <port> : Port for the dashboard server (default 3000)

## Example
bazable ui
