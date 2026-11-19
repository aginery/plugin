# Agent Machinery

Connect your AI harness to [Agent Machinery](https://aginery.com), an MCP gateway for teams deploying AI tools at scale to employee-facing and headless agents. This plugin connects to `https://aginery.com/mcp`; it does not install or run a local server.

## Install

### Cursor

In Cursor, open **Customize → Plugins** and install **Agent Machinery** once it’s available in the Cursor Marketplace. Until then, you can add the server directly with the [Cursor MCP settings](https://cursor.com/docs/mcp): use the name `agent-machinery` and the URL `https://aginery.com/mcp`.

### Claude Code

Run these commands inside Claude Code:

```text
/plugin marketplace add aginery/plugin
/plugin install agent-machinery@aginery
```

Reload plugins if prompted. Use `/mcp` to connect and sign in.

### Codex CLI

```sh
codex plugin marketplace add aginery/plugin
codex plugin add agent-machinery@aginery
```

Start a new Codex session after installing and follow its MCP sign-in prompt.

## Access

Sign in with the account your team uses for Agent Machinery and approve the access you want to grant. Your organization’s setup and your grants determine which tools are available. The plugin does not bundle credentials. Headless workloads should use their own workload identity and the gateway’s client-credentials flow rather than a shared human login.

If you already configured this endpoint directly, remove the old entry when switching to the plugin to avoid loading the server twice.
