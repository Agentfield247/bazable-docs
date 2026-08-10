# bazable init

Creates a `bazable.config.json` file with your project name (from `package.json`) and an empty endpoints list.

## Usage
bazable init

## Options
None.

## What it does
Looks for a package.json in the current directory and reads its name field to set the contract’s projectName. If no package.json is found, defaults to "unknown-project".

Writes a new bazable.config.json with the following structure:

```json
{
  "version": "1.0",
  "projectName": "your-project-name",
  "endpoints": {}
}
The endpoints object starts empty – you’ll populate it with bazable extract, bazable add, or bazable import.

## Safety checks
If bazable.config.json already exists, the command refuses to overwrite it and prints a warning:
⚠ Project already initialized. A bazable.config.json already exists.
This prevents accidental loss of your contract.

## Prerequisites
Your project must be a valid Node.js project with a package.json (optional, but recommended).

The current directory should be the root of your frontend or backend project.


## Example
cd my-frontend
bazable init
