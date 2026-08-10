# bazable ci

Generates a `.github/workflows/bazable.yml` file that runs `bazable inspect` on every pull request to `main`.

## Usage
bazable ci

## Options
-t, --token : Include a BAZABLE_TOKEN secret reference in the workflow. When used, the generated YAML will pass --token ${{ secrets.BAZABLE_TOKEN }} to bazable inspect, enabling headless authentication in CI. (Requires a secret named BAZABLE_TOKEN to be set in your GitHub repository.)

## What it generates
The workflow file (bazable.yml) contains the following steps:

Checkout code – pulls your repository.

Setup Node.js – ensures Node.js 20 is available.

Install Bazable – globally installs bazable-api.

Run contract inspection – executes bazable inspect --ci (or with --token if the --token flag was used).

If bazable inspect exits with a non‑zero code, the pull request is blocked.

## Prerequisites
Your project must contain a valid bazable.config.json.

If you use the --token option, you must first add your Bazable access token as a secret named BAZABLE_TOKEN in your GitHub repository (Settings → Secrets and variables → Actions → New repository secret).

## Example
bazable ci
bazable ci --token
