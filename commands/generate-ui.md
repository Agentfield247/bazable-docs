# bazable gen ui

Generates a React + Tailwind form component from an endpoint’s request schema.

## Usage
bazable gen ui <method> <url>

## Options
- -o, --output <dir> : Output directory (default ./generated-ui)

## Example
bazable gen ui POST https://api.example.com/v1/settlements -o ./my-forms
