# Device Code Authentication

Bazable uses OAuth 2.0 Device Flow for passwordless login.

1. Run any cloud command (push, sync, watch).
2. The CLI prints a clickable link.
3. Open it in your browser; sign in with GitHub or email.
4. The device is approved automatically, and the CLI continues.

No passwords stored. Token is cached locally for future commands.
