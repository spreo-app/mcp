# Spreo MCP Server

Connect AI tools to [Spreo](https://spreo.io), the collaborative whiteboard and meeting platform for agile teams. Once connected, your AI tool can find your workspaces and boards, read what's on them, and create or edit boards for you.

This is a hosted server, so there's nothing to install or run.

```
https://mcp.spreo.io/mcp
```

## Setup

You need a Spreo account. The server uses OAuth, so you sign in with Spreo and choose which account to connect. You don't need an API key.

### Claude

1. Open **Settings > Connectors** and choose to add a custom connector.
2. Enter `https://mcp.spreo.io/mcp` as the URL.
3. Connect, sign in to Spreo, and approve access.

### Claude Code

```bash
claude mcp add --transport http spreo https://mcp.spreo.io/mcp
```

Then run `/mcp` inside Claude Code to sign in.

### Other MCP clients

Add `https://mcp.spreo.io/mcp` as a remote MCP server using the Streamable HTTP transport, and sign in when prompted.

See the [setup guide](https://docs.spreo.io/boards/mcp) for more detail.

## Tools

| Tool | What it does | Access |
| --- | --- | --- |
| `list_workspaces` | Lists your workspaces and folders | Read |
| `list_boards` | Finds boards by search, filter and sort | Read |
| `read_boards` | Reads the content of up to 5 boards | Read |
| `search_people` | Finds people by name or email | Read |
| `edit_board_help` | Returns the guide to editing boards | Read |
| `create_board` | Creates a new blank board | Write |
| `clone_board` | Creates a copy of an existing board | Write |
| `edit_board` | Adds, changes or removes content on a board | Write |

## Permissions

The connection acts as you, in the account you choose when you connect. Your AI tool can only see and change what you can in Spreo.

Account admins can turn off MCP access for their members. You can read more in [permissions and security](https://docs.spreo.io/boards/mcp/mcp-permissions-and-security).

## Support

- **Bugs and feature requests:** [open an issue](https://github.com/spreo-app/mcp/issues)
- **Help:** [Spreo support](https://spreo.io/support)
- **Docs:** [docs.spreo.io/boards/mcp](https://docs.spreo.io/boards/mcp)

## Legal

- [Privacy policy](https://spreo.io/privacy)
- [Terms of service](https://spreo.io/terms)
