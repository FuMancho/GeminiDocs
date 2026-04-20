# Gemini CLI Changelog

> Curated changelog sourced from the [official Gemini CLI releases](https://github.com/google-gemini/gemini-cli/releases).
> Last updated: 2026-04-15

## v0.39.0-preview.0 (Preview)

### Highlights
- **Refactored Subagents and Unified Tooling:** Consolidate subagent tools into a single `invoke_subagent` tool, removed legacy wrapping tools, and improved turn limits for codebase investigator.
- **Advanced Memory and Skill Management:** Introduced `/memory` inbox for reviewing extracted skills and added skill patching support, enhancing agent learning and persistence.
- **Expanded Test and Evaluation Infrastructure:** Added memory and CPU performance integration test harnesses and generalized evaluation infrastructure for better suite organization.
- **Sandbox and Security Hardening:** Centralized sandbox paths for Linux and macOS, enforced read-only security for async git worktree resolution, and optimized Windows sandbox initialization.
- **Enhanced CLI UX and UI Stability:** Improved scroll momentum, added a `debugRainbow` setting, and resolved various memory leaks and PTY exhaustion issues for a smoother terminal experience.

---

## v0.38.1 (Latest Stable)

### Highlights
- **Chapters Narrative Flow:** Introduced tool-based topic grouping ("Chapters") to provide better session structure and narrative continuity in long-running tasks.
- **Context Compression Service:** Implemented a dedicated service for advanced context management, efficiently distilling conversation history to preserve focus and tokens.
- **Enhanced UI Stability & UX:** Introduced a new "Terminal Buffer" mode to solve rendering flicker, along with selective topic expansion and improved tool confirmation layouts.
- **Context-Aware Policy Approvals:** Users can now grant persistent, context-aware approvals for tools, significantly reducing manual confirmation overhead for trusted workflows.
- **Background Process Monitoring:** New tools for monitoring and inspecting background shell processes, providing better visibility into asynchronous tasks.

---

## v0.32.1

### Highlights
- **Plan Mode Enhancements**: Significant updates to Plan Mode, including the ability to open and modify plans in an external editor, adaptations for complex tasks with multi-select options, and integration tests for plan mode.
- **Agent and Steering Improvements**: The generalist agent has been enabled to enhance task delegation, model steering is now supported directly within the workspace, and contiguous parallel admission is enabled for `Kind.Agent` tools.
- **Interactive Shell**: Interactive shell autocompletion has been introduced, significantly enhancing the user experience.
- **Core Stability and Performance**: Extensions are now loaded in parallel, fetch timeouts have been increased, robust A2A streaming reassembly was implemented, and orphaned processes when terminal closes have been prevented.
- **Billing and Quota Handling**: Implemented G1 AI credits overage flow with billing telemetry and added support for quota error fallbacks across all authentication types.

---

## v0.32.0-preview.0 (Preview)

### Highlights
- **Plan Mode Enhancements**: Significant updates to Plan Mode, including support for modifying plans in external editors, adaptive workflows based on task complexity, and new integration tests.
- **Agent and Core Engine Updates**: Enabled the generalist agent, introduced `Kind.Agent` for sub-agent classification, implemented task tracking foundation, and improved Agent-to-Agent (A2A) streaming and content extraction.
- **CLI & User Experience**: Introduced interactive shell autocompletion, added a new verbosity mode for cleaner error reporting, enabled parallel loading of extensions, and improved UI hints and shortcut handling.
- **Billing and Security**: Implemented G1 AI credits overage flow with enhanced billing telemetry, updated the authentication handshake to specification, and added support for a policy engine in extensions.
- **Stability and Bug Fixes**: Addressed numerous issues including 100% CPU consumption by orphaned processes, enhanced retry logic for Code Assist, reduced intrusive MCP errors, and merged duplicate imports across packages.

---

## v0.31.0

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
