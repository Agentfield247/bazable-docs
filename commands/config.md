
#### `docs/commands/config.md`
```markdown
# bazable config

Views or updates the Bazable contract configuration.

## Usage
```bash
bazable config [options]

Options
--get <key> : Print a specific config value (projectName, baseUrl, version, endpoints)

--set-project-name <name> : Set the project name

--set-base-url <url> : Set the base URL

--set-webhook <url> : Set a Slack/Discord webhook URL for push notifications

--set-ai-key <key> : Set an AI API key

--set-ai-base <url> : Set a custom AI API base URL

--set-ai-model <name> : Set the AI model name

Examples

bazable config
bazable config --get baseUrl
bazable config --set-project-name "my-frontend"
