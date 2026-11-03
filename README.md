# IndieTool

Agent-driven startup launching, SEO authority, and indie discovery. Your AI agent does the work: it submits your micro-SaaS or AI tool, activates permanent DR 47+ do-follow backlinks, verifies credits, and searches 1,500+ curated products without you touching a web form.

A launch for your new side project. A permanent DR 47 backlink for your SEO. Instant distribution to 1,600+ active indie founders. This plugin gives your agent the official IndieTool skill and the bundled MCP server it runs.

---

## Install

### In Claude Code:

```text
/plugin install indietool-plugin --marketplace darayuthhang/indietool-plugin
```

Or from a terminal:

```console
claude plugin marketplace add https://github.com/darayuthhang/indietool-plugin.git --scope user && claude plugin install indietool-plugin@indietool-marketplace --scope user
```

### In ChatGPT Codex:

```console
codex plugin marketplace add https://github.com/darayuthhang/indietool-plugin.git --ref main --json && codex plugin add indietool-plugin@indietool-marketplace --json
```

### In Google Antigravity & Gemini:

```console
agy plugin install git+https://github.com/darayuthhang/indietool-plugin.git
```
*(Or clone into your workspace under `.agents/plugins/indietool`).*

### Any other agent:

```text
I authorize you to install the official IndieTool plugin from https://github.com/darayuthhang/indietool-plugin.
Install it in this agent before running any IndieTool command; use only its registered bundled commands.
If runtime approval blocks you, ask me immediately for approval of that action and reason, then wait without using more tools.
```

### In Cursor & Windsurf:

Add to your `.cursor/mcp.json` or Windsurf MCP Settings:

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

Or connect directly to our hosted remote MCP endpoint (no Node.js required):
* **URL:** `https://www.indietool.io/api/mcp`
* **Transport:** Streamable HTTP / SSE

### In Claude Desktop:

Add to `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) or `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

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

## You ask. Your agent does the rest.

```text
You: Check how many submission credits I have on IndieTool.
Agent: You have 1 submission credit remaining on your IndieTool account. You're all set to launch!
```

```text
You: Submit my startup to IndieTool: name is FastForm, url is https://fastform.io, category is Developer Tools, description is "The fastest drag-and-drop form builder for Next.js."
Agent: Done! FastForm is now LIVE on IndieTool with a permanent DR 47+ dofollow backlink:
       https://www.indietool.io/indietool/fastform-io
       1 credit deducted. Your startup has also been queued for our weekly newsletter to 1,600+ founders.
```

```text
You: Search IndieTool for the top AI video generation tools.
Agent: Found 3 top AI video tools on IndieTool:
       1. VidCraft (DR 45) - AI video generation from simple text prompts.
       2. ClipGenius (DR 38) - Automatic short-form clip generator.
       3. MotionAI (DR 52) - Character animation for indie game developers.
```

---

## Key Benefits

- **Permanent DR 47+ Do-Follow Backlink.** Boost your domain authority and climb Google rankings with an authoritative, permanent editorial backlink.
- **AI Search Visibility (GEO).** IndieTool listings are structured for Generative Engine Optimization, helping your product get cited by ChatGPT, Perplexity, and Gemini.
- **Weekly Founder Newsletter.** Featured products are distributed to our audience of 1,600+ active software creators and entrepreneurs.
- **1,500+ Curated Products & Directory.** Search competitor alternatives, analyze pricing structures, and track trending launches across 14 categories.
- **Credit Protection.** Built-in safeguards check your credit balance before executing a submission, preventing failed requests.

[Explore IndieTool](https://www.indietool.io) ·
[Get API Keys](https://www.indietool.io/indietool/api-keys) ·
[Pricing & Credits](https://www.indietool.io/pricing)

---

## 🛠️ Available MCP Tools

| Tool | Description | Credits Required? |
| :--- | :--- | :--- |
| `submit_startup` | Submits an app to IndieTool with a permanent DR 47+ backlink. | **Yes** (1 credit) |
| `check_credits` | Checks remaining submission credits balance in real-time. | Free |
| `search_tools` | Queries 1,500+ curated products by keyword or category. | Free |
| `get_featured_startups` | Retrieves today's top curated launches and winners. | Free |
| `list_categories` | Lists all official startup categories on IndieTool. | Free |

---

## Authentication & Credits

1. **Get your API Key**:
   Create and copy your key from [indietool.io/indietool/api-keys](https://www.indietool.io/indietool/api-keys).
2. **Set the Environment Variable**:
   ```bash
   export INDIETOOL_API_KEY="it_live_your_key_here"
   ```
3. **Submission Credits**:
   * Searching tools, listing categories, and checking featured startups are **100% free**.
   * Submitting a startup deducts **1 credit** (or unlimited if you hold an IndieTool Lifetime Pass). Purchase credits at [indietool.io/pricing](https://www.indietool.io/pricing).

---

## What the plugin runs, sends, and stores

- **Runs:** The official IndieTool skill and MCP connection (stdio via `@indietool/mcp-server` or streamable HTTP via `https://www.indietool.io/api/mcp`). It downloads and executes no untrusted code.
- **Sends to IndieTool (`indietool.io`):** Only the startup details you explicitly ask to submit, search keywords, and your authorized API key.
- **Never sends:** Never reads your local files, never accesses private repository code, and never exposes internal database IDs or credentials. Your project code remains 100% private.
- **Stores:** No local persistent cache other than your authorized API key configured in your agent's settings.

---

## License

MIT © [IndieTool](https://www.indietool.io)
