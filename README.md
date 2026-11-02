# IndieTool Universal MCP Server & Plugin 🚀

The official [IndieTool](https://www.indietool.io) Model Context Protocol (MCP) server and plugin for **Claude Desktop**, **Cursor IDE**, **ChatGPT**, **Grok**, and **Google Antigravity**.

Allows AI agents to:
- 🚀 **Submit Startups with Backlinks**: Submit apps directly from chat to get a permanent DR 47+ do-follow backlink.
- 💳 **Check Submission Credits**: Verify available submission credits in real-time.
- 🔍 **Search 1,500+ Indie Tools**: Find curated SaaS apps, AI tools, competitor alternatives, and founder products.
- 🏆 **Daily Launch Winners**: Surface today's top featured startups and products.
- 📂 **Official Categories**: Explore standard software and startup categories.

---

## ⚡ Quick Start: Connect to Your Favorite AI

### 1. 🟣 Claude Desktop
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

### 2. 💻 Cursor IDE / Windsurf
In **Cursor**:
1. Open **Settings** → **Features** → **MCP**.
2. Click **+ Add New MCP Server**.
3. Fill in:
   * **Name:** `indietool`
   * **Type:** `command`
   * **Command:** `npx -y @indietool/mcp-server`
   * **Environment Variables:** `INDIETOOL_API_KEY=it_live_your_api_key_here`

In **Windsurf**:
Open **Settings** → **Cascade** → **MCP Servers** and add the configuration above.

---

### 3. 🔵 Google Antigravity & Gemini Agents
Install directly via the Antigravity CLI:
```bash
agy plugin install git+https://github.com/darayuthhang/indietool-plugin.git
```
Or add the plugin directly to your workspace under `.agents/plugins/indietool`.

---

### 4. 🟢 ChatGPT & Grok (Agents / MCP Clients)
For OpenAI / Grok agent frameworks and MCP-compatible chat interfaces, run via `npx`:
```bash
npx -y @indietool/mcp-server
```
Pass `INDIETOOL_API_KEY` as an environment variable or header token.

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
