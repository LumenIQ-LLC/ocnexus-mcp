# OCNexus MCP

Connect Cursor, Grok and other MCP clients to your OCNexus account.

**Publisher:** OCNexus (by LumenIQ)

This repository is a thin configuration wrapper for installing the hosted OCNexus MCP server. It contains no server code and no secrets.

## What it does

With an OCNexus subscription, your MCP client can:

- Show your OCNexus identity and plan.
- List the repositories your account is authorized to work on.
- Submit an authorized repository to Forge.
- Check Forge run status, findings and run history.

## Requirements

- An OCNexus Starter or Pro subscription.
- An MCP client that supports remote MCP servers with sign-in.

## Install

The hosted server is at:

```
https://mcp.ocnexus.dev/subscriber
```

- **Cursor:** this repository is packaged as a Cursor plugin (`.cursor-plugin/plugin.json`).
- **Other MCP clients:** use the server entry in `mcp.json` (client id `grok-subscriber`), or add the URL above as a remote MCP server in your client.

On first use, sign in with your OCNexus account and approve the requested permissions.

## Permissions

| Permission | What it allows |
|---|---|
| `ocn:profile:read` | Read your OCNexus identity and plan. |
| `ocn:repo:read` | List the repositories your account is authorized for. |
| `ocn:forge:read` | Read Forge run status, findings and run history. |
| `ocn:forge:submit` | Submit an authorized repository to Forge. |
| `ocn:usage:read` | Reserved for usage reporting. No tool uses it yet. |

Each permission is granted when you approve it at sign-in. Your client only lists the tools that your approved permissions allow.

## Security

- No secrets are stored in this repository. Do not add credentials or tokens to `mcp.json`.
- Access is tied to your OCNexus account through sign-in.
- To report a security issue, use the contact options at https://ocnexus.dev.

## Links

- https://ocnexus.dev
- https://portal.ocnexus.dev

## License

MIT. See [LICENSE](LICENSE).
