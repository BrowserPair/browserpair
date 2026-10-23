# BrowserPair MCP Registry metadata

This directory prepares the remote-server listing for the official MCP Registry. **Not published yet.** Committing this file does not create a registry listing.

The candidate name is `com.browserpair/browserpair`. Its reverse-domain namespace should be authenticated through BrowserPair's domain before publication. The production server remains `https://mcp.browserpair.com`; its private implementation is not included here.

## Review before publication

1. Search the live registry for BrowserPair and the exact remote URL. Reuse an existing owned listing if one appears; do not create a competing identity.
2. Validate `server.json` against its pinned official schema with the current publisher CLI.
3. Confirm the public HTTPS endpoint and OAuth discovery still work.
4. Authenticate the domain namespace using the official DNS or HTTP procedure. Keep publisher private keys and login tokens outside Git.
5. Publish with `mcp-publisher publish registry/server.json` after publication approval, then read the entry back from the production registry.
6. Record the returned server name, version, and verified listing URL here. Registry versions are separate from extension and application versions.

The listing uses only a remote transport. No package entry or public copy of the application source is needed.

Official references: [remote servers](https://github.com/modelcontextprotocol/registry/blob/main/docs/modelcontextprotocol-io/remote-servers.mdx), [authentication](https://github.com/modelcontextprotocol/registry/blob/main/docs/modelcontextprotocol-io/authentication.mdx), and [publisher commands](https://github.com/modelcontextprotocol/registry/blob/main/docs/reference/cli/commands.md).
