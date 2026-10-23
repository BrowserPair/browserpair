# BrowserPair MCP Registry metadata

This directory tracks BrowserPair's published remote-server listing in the official MCP Registry.

- Name: `com.browserpair/browserpair`
- Version: `1.0.0`
- Status verified: **active**, latest version
- Published: October 23, 2026
- [Live registry record](https://registry.modelcontextprotocol.io/v0.1/servers/com.browserpair%2Fbrowserpair/versions/latest)

The listing was read back from the production API after publication. The publisher CLI and official JSON schema both validated the manifest. Committing metadata alone does not publish registry updates.

The name `com.browserpair/browserpair` uses BrowserPair's reverse-domain namespace. Domain ownership was authenticated using the Registry's DNS proof procedure. The production server remains `https://mcp.browserpair.com`; its private implementation is not included here.

## Future updates

1. Search the live registry for BrowserPair and the exact remote URL. Reuse an existing owned listing if one appears; do not create a competing identity.
2. Validate `server.json` against its pinned official schema with the current publisher CLI.
3. Confirm the public HTTPS endpoint and OAuth discovery still work.
4. Authenticate the domain namespace using the official DNS or HTTP procedure. Keep publisher private keys and login tokens outside Git.
5. Increment the manifest version and publish with `mcp-publisher publish registry/server.json` after publication approval, then read the entry back from the production registry.
6. Update the version and verified listing URL here. Registry versions are separate from extension and application versions.

The one-time signing key, login token, and temporary DNS proof used for initial publication were removed afterward. Future publication should generate a fresh proof or use another approved namespace authentication method.

The listing uses only a remote transport. No package entry or public copy of the application source is needed.

Official references: [remote servers](https://github.com/modelcontextprotocol/registry/blob/main/docs/modelcontextprotocol-io/remote-servers.mdx), [authentication](https://github.com/modelcontextprotocol/registry/blob/main/docs/modelcontextprotocol-io/authentication.mdx), and [publisher commands](https://github.com/modelcontextprotocol/registry/blob/main/docs/reference/cli/commands.md).
