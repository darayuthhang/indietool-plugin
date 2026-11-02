# IndieTool Plugin Rules

1. **Credit Enforcement First**:
   - Never call `submit_startup` without verifying that the user has at least 1 credit or a Lifetime Pass.
   - If a user has 0 credits, explain politely and direct them to `https://www.indietool.io/pricing`.

2. **Accurate App Metadata**:
   - Ensure the `websiteUrl` is a valid, clean HTTPS URL.
   - Match categories to official IndieTool categories using `list_categories`.
   - Never invent or fabricate statistics (domain rating, backlink status).

3. **Privacy & Security**:
   - Never log, display, or store full unmasked API keys or user account IDs in public text.

