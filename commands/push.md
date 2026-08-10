# bazable push

Uploads the local contract to Bazable Cloud. Creates a cloud project on first push.

## Usage
bazable push

## Prerequisites
Your project must be initialized (bazable init) and contain a valid bazable.config.json with at least one endpoint.

You must be authenticated. If you're not logged in, the command will automatically start the device‑code flow—open the printed link, sign in with GitHub or email, and the push continues.

## What it does
Checks authentication – if no stored token exists, starts the device‑code flow.

Creates a cloud project – on the very first push, a unique project ID (bz_proj_…) is generated and saved to your bazable.config.json as cloudProjectId. The cloud API base URL is also saved automatically.

Uploads the contract – your entire contract (endpoints, schemas, base URLs) is sent to the cloud and stored as a new version.

Versioning – each push increments the version number. You can later roll back to a specific version with bazable sync --version <number>.

Webhook notification – if you've set a webhook URL (bazable config --set-webhook), a notification is sent to your Slack/Discord channel.

After the first push, teammates can simply clone the repository and run bazable sync to pull the latest contract—no additional configuration needed.

## Options
None.

## Example
bazable push
