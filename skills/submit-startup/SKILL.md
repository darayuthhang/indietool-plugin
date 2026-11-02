---
name: submit-startup
description: Submit an indie app or startup to IndieTool.io with a permanent DR 47+ backlink. Enforces mandatory credit verification before launching.
---

# Submit Startup to IndieTool

Use this skill when the user asks to launch, list, publish, or submit their web app, SaaS, or startup to IndieTool (`indietool.io`).

## Workflow

### Step 1: Check Submission Credits First
Always call the `check_credits` MCP tool before attempting submission:
* If the user has **0 credits** and no Lifetime Pass:
  - Do NOT call `submit_startup`.
  - Explain that IndieTool requires an active submission credit.
  - Direct the user to purchase credits: [IndieTool Pricing](https://www.indietool.io/pricing)
  - Direct the user to manage their API keys: [IndieTool API Keys](https://www.indietool.io/indietool/api-keys)

* If the user has **1 or more credits** or an active **Lifetime Unlimited Pass**:
  - Proceed to Step 2.

### Step 2: Validate Required Submission Details
Collect or verify the following required inputs:
* `websiteUrl`: The full URL of the project (e.g. `https://mytool.com`).
* `appName`: Clean name of the project.
* `category`: One of the official IndieTool categories (`Developer Tools`, `Ai`, `Marketing`, `Fintech`, `Design`, `Productivity`, `E-Commerce`, etc.).
* `description`: Concise 1-2 sentence pitch explaining what problem it solves.
* `imageUrl`: (Optional) Direct URL to the app's logo or preview icon.

### Step 3: Call `submit_startup`
Invoke the `submit_startup` MCP tool with the verified details.
Upon successful submission:
* Provide the live IndieTool URL (`https://www.indietool.io/indietool/<domain>`).
* Confirm that 1 credit was deducted and report remaining credits.
* Highlight that the DR 47+ do-follow backlink is now active.

