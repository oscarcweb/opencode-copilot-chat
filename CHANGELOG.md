# Changelog

All notable changes to the **OpenCode Go BYOK Provider** extension are documented here.

## [0.1.1] — 2026-05-14

### Fixed
- Switched the Language Models gear flow to VS Code's native provider configuration schema.
- Added `apiKey` as a secret provider configuration field so configure/add prompts proceed from **Group Name** to **OpenCode Go API Key**.
- Provider now reads the configured API key from VS Code's language model configuration, with the command-stored key kept as a fallback.

## [0.1.0] — 2026-05-14

### Added
- Initial public release on VS Code Marketplace
- Live model list fetched from `https://opencode.ai/zen/go/v1/models` on activation
- Bundled fallback model metadata table (context window + max output tokens per model)
- Dual endpoint routing: OpenAI-compatible `/chat/completions` for standard models, Anthropic-compatible `/messages` for MiniMax M2 models
- Tool-calling support forwarded to both endpoint types
- `OpenCode Go: Manage Provider` command — model selection and management dialog
- `OpenCode Go: Set API Key` command — stores API key in VS Code Secret Storage
- `OpenCode Go: Diagnostics` command — renders a markdown report of all registered models
- Settings: `opencodego.temperature`, `opencodego.maxTokens`, `opencodego.maxInputTokens`
- Per-model token limit overrides via `opencodego.maxInputTokens` and `opencodego.maxTokens`
