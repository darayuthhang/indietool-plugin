# IndieTool Universal MCP Server & Plugin 🚀

The official [IndieTool](https://www.indietool.io) Model Context Protocol (MCP) server and agent plugin for **Google Antigravity**, **xAI Grok Build**, **OpenAI Codex**, **Claude Code**, and **Cursor IDE**.

Allows AI coding assistants and agents to:
- 🚀 **Submit Startups with Backlinks**: Submit apps directly from chat to get a permanent DR 47+ do-follow backlink.
- 💳 **Check Submission Credits**: Verify available submission credits in real-time.
- 🔍 **Search 1,500+ Indie Tools**: Find curated SaaS apps, AI tools, competitor alternatives, and founder products.
- 🏆 **Daily Launch Winners**: Surface today's top featured startups and products.
- 📂 **Official Categories**: Explore standard software and startup categories.

---

## ⚡ Quick Start: Install in Terminal AI Agents

Install IndieTool into your terminal agent with a single command:

### 🔵 Google Antigravity (`agy`)
```bash
agy plugin install git+https://github.com/darayuthhang/indietool-plugin.git
```
*(Or in the Antigravity TUI, type `/plugin` to manage).*

---

### 🔴 xAI Grok Build (`grok`)
```bash
grok plugin install indietool --trust
```
*(Or inside the interactive Grok Build terminal, type `/marketplace` or `/mcps`).*

---

### 🟢 OpenAI Codex CLI (`codex`)
```bash
codex plugin marketplace add darayuthhang/indietool-plugin --ref main
```
*(Or inside the interactive Codex terminal, type `/plugins`).*

---

### 🟣 Anthropic Claude Code (`claude`)
```bash
claude mcp add indietool npx -y @indietool/mcp-server
```

---

## 💻 Install in AI Editors & Desktop Apps

### 1. Cursor IDE & Windsurf
In **Cursor**:
1. Open **Settings** → **Features** → **MCP**.
2. Click **+ Add New MCP Server**:
   * **Name:** `indietool`
   * **Type:** `command`
   * **Command:** `npx -y @indietool/mcp-server`
   * **Environment Variables:** `INDIETOOL_API_KEY=it_live_your_api_key_here`

In **Windsurf**:
Open **Settings** → **Cascade** → **MCP Servers** and add the configuration above.

---

### 2. Claude Desktop
Add this to your Claude configuration file:
* **macOS:** `~/Library/Application Support/Claude/claude_desktop_config.json`
* **Windows:** `%APPDATA%\Claude\claude_desktop_config.json`

```json
{
  "mcpServers": {
    "indietool": {
      "command": "npx",
      "args": ["-y", "@indietool/mcp-server"],
      "env": {
        "INDIETOOL_API_KEY": "it_live_your_api_key_here"
      }
    }
  }
}
```

---

## 🔑 Authentication & Credits

1. **Get your API Key**:
   Copy your API key from [https://www.indietool.io/indietool/api-keys](https://www.indietool.io/indietool/api-keys).
2. **Submission Credits**:
   * Searching tools, listing categories, and checking featured startups are **100% free** and require no credits.
   * Submitting a startup deducts **1 credit** (or unlimited if you hold an IndieTool Lifetime Pass). Purchase credits at [indietool.io/pricing](https://www.indietool.io/pricing).

---

## 🛠️ Available MCP Tools

| Tool | Description | Requires Credits? |
| :--- | :--- | :--- |
| `submit_startup` | Submits an app to IndieTool with a permanent DR 47+ backlink. | **Yes** (1 credit) |
| `check_credits` | Checks remaining submission credits balance in real-time. | No |
| `search_tools` | Queries 1,500+ curated products by keyword or category. | No |
| `get_featured_startups`| Retrieves today's top featured launches and winners. | No |
| `list_categories` | Lists all official startup categories. | No |

---

## 📄 License

MIT © [IndieTool](https://www.indietool.io)
