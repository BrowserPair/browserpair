<p align="center"><img src="https://browserpair.com/mark.svg" width="72" alt="BrowserPair logo"></p>

# BrowserPair — AI agents in your signed-in Chrome

BrowserPair connects ChatGPT, Claude and custom AI agents to the Chrome profile you already use. Give each agent bounded access to websites and actions, review approvals when needed, and verify the outcome.

**This is the official product and community hub. The application source is private and maintained separately.**

[Start free](https://app.browserpair.com/) · [Website](https://browserpair.com/) · [Documentation](https://docs.browserpair.com/) · [Chrome extension](https://chromewebstore.google.com/detail/agdomhjeahcbelohnmjmbldeldclnoof) · [Changelog](https://browserpair.com/changelog/)

## Get started

1. Install the [Chrome extension](https://chromewebstore.google.com/detail/agdomhjeahcbelohnmjmbldeldclnoof) and pair your browser in the [BrowserPair app](https://app.browserpair.com/).
2. Choose a connection: [ChatGPT](https://docs.browserpair.com/chatgpt), [Claude](https://docs.browserpair.com/claude), [another AI app](https://docs.browserpair.com/connect-ai-app), [Remote MCP](https://docs.browserpair.com/remote-mcp), or [REST](https://docs.browserpair.com/rest-api).
3. Define the browser, websites and capabilities the agent may use.
4. Start a small task. Review any approval request and inspect the result.

For tasks started inside BrowserPair, configure your own Agent Model. An external MCP agent remains the Agent Model and does not require that managed-model setup. Read the [quickstart](https://docs.browserpair.com/quickstart) for the current UI.

## What can I use it for?

| Task | Useful result | Boundary |
| --- | --- | --- |
| Research and product comparisons | Source-linked comparison with prices, dates and uncertainties | No purchase implied |
| Work in an authenticated dashboard | Read visible statuses and summarize findings | Only authorized websites and data |
| Prepare a form | Fill a user-provided draft and surface validation errors | Review before submission |
| Repeat a documented workflow | Follow a reusable Skill with evidence at each important step | A Skill never adds authority |

Capabilities depend on the website, the agent and your granted permissions. These are workflow examples, not guarantees for every site.

## How BrowserPair works

- **Your Chrome:** signed-in sessions remain in your browser profile; the extension observes pages and performs browser actions.
- **Scoped access:** the agent key and task limit browsers, websites and capabilities.
- **Human approval:** protected actions and runtime permission requests pause for the user.
- **Durable tasks:** task identity and state survive normal reconnects.
- **Outcome verification:** uncertain effects are checked before another attempt.

BrowserPair Cloud coordinates accounts, permissions, routing, approvals, usage and task state. Task observations may be processed by the connected AI provider. Existing browser sessions staying on-device does not mean every piece of task data stays local. See [Security](https://browserpair.com/security), [Privacy](https://browserpair.com/privacy) and [Sensitive access](https://docs.browserpair.com/sensitive-access).

## BrowserPair or Playwright?

Use BrowserPair when your own signed-in profile and user-controlled agent authority are central to the workflow. Use Playwright when you need programmable tests, isolated browser contexts or deterministic CI automation. They serve different needs; choose by the session and verification requirements.

Read the [BrowserPair, Playwright, and Browser Use comparison](https://docs.browserpair.com/compare-browser-automation) for existing-session support and integration choices.

## Public resources

- [Documentation](https://docs.browserpair.com/): setup, permissions, task semantics and API reference.
- [Examples](https://github.com/BrowserPair/examples): minimal integration code and connection recipes.
- [Skills](https://github.com/BrowserPair/skills): reusable task knowledge and verification checklists.
- [Awesome browser agents](https://github.com/BrowserPair/awesome-browser-agents): tools, frameworks and evaluation resources across the ecosystem.

## Guides and integration metadata

- [Browser sessions and data flow](https://docs.browserpair.com/browser-session-data-flow): what stays in Chrome and what observations can reach an AI provider.
- [Read an authenticated dashboard](https://docs.browserpair.com/read-authenticated-dashboard): a bounded workflow for ChatGPT or Claude.
- [Official MCP Registry entry](https://registry.modelcontextprotocol.io/v0.1/servers/com.browserpair%2Fbrowserpair/versions/latest): `com.browserpair/browserpair`, remote Streamable HTTP.
- [Product facts](./product.json) and [registry metadata](./registry/): maintained public integration references.

## Frequently asked questions

**Does BrowserPair include an AI subscription?**

Your AI app or configured model provider supplies the model. Check [pricing](https://browserpair.com/pricing) for current BrowserPair limits and billing.

**Can a web page or Skill grant more permissions?**

No. Page content, screenshots, model output and Skills cannot expand the user's authority.

**What happens after a disconnect or an uncertain click?**

Read the current task state and obtain fresh evidence. Do not blindly repeat a potentially completed action. See [task semantics](https://docs.browserpair.com/task-semantics).

**Is BrowserPair open source?**

The public resources in this organization are available under their own licenses. The hosted product and extension source are maintained privately.

## Help and feedback

Use this repository's Issues for reproducible public product reports and feature requests. Include the expected behavior, actual behavior, browser/extension version and redacted reproduction steps. Do not post agent keys, cookies, account identifiers, private page content or unredacted logs.

Use [Support](https://browserpair.com/support) for account-specific questions and security reporting. Check [service status](https://status.browserpair.com/) before reporting an outage.

Contributions to docs, examples and Skills belong in their respective repositories.
