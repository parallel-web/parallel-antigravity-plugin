# Parallel for Antigravity

Search the web and read pages from Antigravity with Parallel. This plugin provides
`web_search` and `web_fetch` through the hosted Parallel Search MCP server.
No Parallel account, API key, or Parallel CLI is required.

## Install

With the [Antigravity CLI](https://antigravity.google/docs/cli/install) installed:

```bash
agy plugin install https://github.com/parallel-web/parallel-antigravity-plugin
agy plugin list --json
```

The plugin connects directly to Parallel's hosted Search MCP server. There is
no Parallel sign-in or API key to configure. Antigravity may ask you to approve
tool calls.

### Install from a local checkout

```bash
git clone https://github.com/parallel-web/parallel-antigravity-plugin.git parallel
cd parallel
agy plugin validate . --strict
agy plugin install .
agy plugin list --json
```

The plugin is named `parallel` and contains one MCP server. It does not include
skills, agents, or hooks. If you already have a separate Parallel MCP connection,
keep only one enabled to avoid duplicate tools.

## Get started

Open **Customizations → Installed → Parallel** and choose a starter prompt.
Select your project before sending. For a feature or error question, add the
feature description or exact error so Antigravity has the context it needs.

You can ask Antigravity to find current documentation, look up an error, or read
a webpage. Tool activity should show Parallel's `web_search` or `web_fetch`.
Antigravity may ask you to approve a tool call.

## Privacy and support

Tool calls send search queries, objectives, requested URLs, and optional session
metadata to Parallel. The plugin configures no authentication headers or local
commands. Anonymous access is subject to free-tier rate limits.

See the [Search MCP documentation](https://docs.parallel.ai/search/search-mcp),
[Privacy Policy](https://parallel.ai/privacy-policy), and
[Customer Terms](https://parallel.ai/customer-terms).
For help, email [support@parallel.ai](mailto:support@parallel.ai).

To uninstall:

```bash
agy plugin uninstall parallel
```
