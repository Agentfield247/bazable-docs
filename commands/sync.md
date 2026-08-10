# bazable sync

Pulls the latest contract from Bazable Cloud and overwrites the local `bazable.config.json`.

## Usage
bazable sync

## Options
--version <v> : Fetch a specific contract version instead of the latest.

-t, --token <token> : Use a specific access token (headless mode, no browser authentication).

## Prerequisites
Your bazable.config.json must contain a cloudProjectId (set automatically by the first bazable push).

You must be authenticated. If you're not logged in, the command will start the device‑code flow automatically. In CI environments, use --token to authenticate headlessly.

## What it does
Checks authentication – if no stored token exists (and no --token is provided), starts the device‑code flow.

Fetches the contract – retrieves the contract data from the cloud. By default it gets the latest version, but you can specify --version 3 to roll back to version 3.

Overwrites the local contract – your local bazable.config.json is replaced with the fetched version. All endpoints, schemas, base URLs, and the projectName are updated.

Handles missing versions – if the requested version doesn't exist, a clear error is shown.

## Example
bazable sync

#Roll back to version 1:
bazable sync --version 1

#Use headless authentication in CI (with a token stored as a secret):
bazable sync --token $BAZABLE_TOKEN
