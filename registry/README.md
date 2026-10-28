# BrowserPair MCP Registry metadata

This repository includes the public metadata for BrowserPair's official remote MCP server.

- Server: `com.browserpair/browserpair`
- Version: `1.0.0`
- Endpoint: `https://mcp.browserpair.com`
- [Current listing in the official MCP Registry](https://registry.modelcontextprotocol.io/v0.1/servers/com.browserpair%2Fbrowserpair/versions/latest)

The registry entry describes how clients connect to the hosted service. It does not publish BrowserPair's application or extension source code.

## Updating the listing

1. Verify the existing registry entry and production endpoint.
2. Validate [server.json](server.json) against the current official schema.
3. Publish an approved version with the official MCP Registry tooling.
4. Verify the new version appears in the live registry before updating this page.

Registry versions are independent of BrowserPair's extension and application versions. Authentication and operational procedures are maintained privately.

[Remote MCP documentation](https://docs.browserpair.com/remote-mcp) · [MCP Registry](https://registry.modelcontextprotocol.io/)
