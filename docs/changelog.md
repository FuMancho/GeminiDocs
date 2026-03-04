# Gemini CLI Changelog

> Curated changelog sourced from the [official Gemini CLI releases](https://github.com/google-gemini/gemini-cli/releases).
> Last updated: 2026-03-04

## v0.33.0-preview.0 (Preview)

### Highlights
- **Plan Mode Enhancements**: Added support for annotating plans with feedback for iteration, enabling built-in research subagents in plan mode, and a new `copy` subcommand.
- **Agent and Skill Improvements**: Introduced the new `github-issue-creator` skill, implemented HTTP authentication support for A2A remote agents, and added support for authenticated A2A agent card discovery.
- **CLI UX/UI Updates**: Redesigned the header to be compact with an ASCII icon, inverted the context window display to show usage, and directly indicate auth required state for agents.
- **Core and ACP Enhancements**: Implemented slash command handling in ACP (for `/memory`, `/init`, `/extensions`, and `/restore`), added a set models interface to ACP, and centralized `read_file` limits while truncating large MCP tool output.

---

## v0.32.0-preview.0 (Preview)

### Highlights
- **Plan Mode Enhancements**: Significant updates to Plan Mode, including support for modifying plans in external editors, adaptive workflows based on task complexity, and new integration tests.
- **Agent and Core Engine Updates**: Enabled the generalist agent, introduced `Kind.Agent` for sub-agent classification, implemented task tracking foundation, and improved Agent-to-Agent (A2A) streaming and content extraction.
- **CLI & User Experience**: Introduced interactive shell autocompletion, added a new verbosity mode for cleaner error reporting, enabled parallel loading of extensions, and improved UI hints and shortcut handling.
- **Billing and Security**: Implemented G1 AI credits overage flow with enhanced billing telemetry, updated the authentication handshake to specification, and added support for a policy engine in extensions.
- **Stability and Bug Fixes**: Addressed numerous issues including 100% CPU consumption by orphaned processes, enhanced retry logic for Code Assist, reduced intrusive MCP errors, and merged duplicate imports across packages.

---

## v0.31.0 (Latest Stable)

### Highlights
- **Gemini 3.1 Pro Preview**: Support for the new Gemini 3.1 Pro Preview model
- **Experimental Browser Agent**: New browser agent for direct web page interaction and context retrieval
- **Policy Engine Updates**: Project-level policies, MCP server wildcards, tool annotation matching
- **Web Fetch Enhancements**: Experimental direct web fetch tool with rate-limiting
- **Improved Plan Mode**: Custom storage directories, automatic model switching, post-execution summarization

### Notable Changes
- Ranged reads, limited searches, and fuzzy editing improvements (#19240)
- `gemini --resume` hint on exit (#16285)
- Alt+D for forward word deletion (#19300)
- macOS run-event notifications in interactive mode (#19056)
- MCP progress updates support (#19046)
- Devtools package migrated into monorepo (#18936)
- Admin settings only apply when `adminControlsApplicable = true` (#19453)
- `/dir add` directories included in @ autocomplete suggestions (#19246)
- Experimental in-progress steering hints (#19307)
- Plan mode documentation (#19467)

### Bug Fixes
- Fix bottom border color (#19266)
- Optimize height calculations for ask_user dialog (#19017)
- Support legacy onConfirm callback in ToolActionsContext (#19369)
- Plan mode safe fallback when experiment setting not enabled (#19439)
- Prevent empty history items (#19014)
- Ensure directory exists before writing conversation file (#18429)
- Ripgrep flag pattern fix (#18858)
- Disable auto-completion on Shift+Tab to preserve mode cycling (#19451)
- Unknown slash commands treated as regular input (#17393)

---

## v0.30.0

*See [full changelog](https://geminicli.com/docs/changelogs/) for earlier versions.*
