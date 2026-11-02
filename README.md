# IndieTool Antigravity Plugin 🚀

The official [IndieTool](https://www.indietool.io) plugin for Google Antigravity and Gemini agents.

Allows AI agents to:
- 💳 **Check Submission Credits**: Check available credits in real-time.
- 🚀 **Submit Startups & Apps**: Deduct 1 credit and launch live with a permanent DR 47+ do-follow backlink.
- 🔍 **Search Indie Tools**: Query 1,500+ curated indie apps, SaaS alternatives, and startups.
- 🏆 **Featured Launches**: Retrieve today's top curated launches and winners.
- 📂 **Categories**: Browse all official software categories.

---

## 📦 Installation

### Option 1: One-Click Marketplace Card
If installed via the Google Agent Marketplace:
```html
<plugin-card catalog-id="indietool"></plugin-card>
```

### Option 2: CLI Git Install
Install directly from GitHub:
```bash
agy plugin install git+https://github.com/darayuthhang/indietool-plugin.git
```

### Option 3: Workspace Staging
Clone or copy this folder into your project's `.agents/plugins/indietool` directory:
```bash
git clone https://github.com/darayuthhang/indietool-plugin.git .agents/plugins/indietool
```

---

## 🔑 Authentication

To use tools that interact with your account (like checking credits or submitting startups):

1. **Obtain an API Key**:
   Create or copy your API key from [https://www.indietool.io/indietool/api-keys](https://www.indietool.io/indietool/api-keys).

2. **Set Environment Variable**:
   Set `INDIETOOL_API_KEY` in your terminal shell or environment:
   ```bash
   export INDIETOOL_API_KEY="it_live_your_key_here"
   ```

---

## 🛠️ Included Components

### MCP Server (`mcp_config.json`)
Exposes the `@indietool/mcp-server` running via `npx` with:
- `check_credits`
- `submit_startup`
- `search_tools`
- `get_featured_startups`
- `list_categories`

### Skills (`skills/`)
- `search-indietool`: Guides the agent to query tools, compare software, and surface daily launch winners.
- `submit-startup`: Enforces credit verification checks before submitting apps to prevent failed launches.

### Rules (`rules/AGENTS.md`)
- Enforces credit verification prior to launching.
- Ensures accurate URLs and official category mappings.
- Forbids logging or exposing secret API keys.
