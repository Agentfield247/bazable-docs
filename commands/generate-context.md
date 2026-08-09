# bazable gen context

Generates AI agent context files in your project root so that AI coding tools (Cursor, Cline, Roo Code) automatically respect your Bazable contract.

## Usage
```bash
bazable gen context


Generate a React + Tailwind form using AI:
bazable gen ui POST https://api.example.com/v1/settlements --ai --framework react-tailwind
---

## 2. Update the existing UI generator page: `docs/commands/generate-ui.md`

Replace its content with:

```markdown
# bazable gen ui

Generates a form component from an endpoint’s request schema.  
By default, produces a **zero‑dependency, standalone HTML file** with embedded CSS and JavaScript.  
You can also use `--ai` to let an LLM generate the UI for any framework.

## Usage
```bash
bazable gen ui <method> <url> [options]
