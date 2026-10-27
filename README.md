# BRICO releases

Release binaries for **BRICO**: your feature memory. BRICO finds the features
you've built in your other projects, tells you how well each fits the project
you're in, and lets your coding agent wire it in.

This repository holds release downloads only. Docs: https://www.bricowerx.com

## Install

```sh
npm i -g bricowerx
# or
curl -fsSL https://github.com/ScienceWerx-Inc/brico_release/releases/latest/download/install.sh | sh
```

## Use it in your coding agent (MCP)

```sh
brico login bt_…                               # your BRICO Builder invite token
brico index ~/code/an-old-project              # remember its features
claude mcp add brico -- npx -y bricowerx mcp   # Claude Code
```

Cursor, in `~/.cursor/mcp.json`:

```json
{ "mcpServers": { "brico": { "command": "npx", "args": ["-y", "bricowerx", "mcp"] } } }
```

Every release includes `SHA256SUMS.txt`; the installers verify downloads against it.
