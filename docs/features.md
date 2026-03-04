# Features & Capabilities

An overview of the core features that make Gemini CLI a powerful agentic coding assistant.

## Plan Mode

Switch to read-only Plan Mode to have Gemini analyze your project and produce a structured plan before making any changes:

```text
/plan
```

> [!NOTE]
> Plan Mode requires the `experimental.plan` setting to be enabled.

See [Plan Mode documentation](https://geminicli.com/docs/cli/plan-mode/).

## Skills

Skills provide on-demand expertise and specialized workflows. They appear as slash commands when invoked.

```text
/skills list         # List all discovered skills
/skills enable <name>
/skills disable <name>
/skills reload       # Refresh from all tiers
```

Create custom skills at the workspace (`<project>/.gemini/skills/`) or user (`~/.gemini/skills/`) level. See [Creating Skills](https://geminicli.com/docs/cli/creating-skills).

## Checkpointing & Rewind

Gemini CLI automatically creates Git checkpoints before modifying files, allowing safe rollback:

```text
/restore             # List checkpoints and restore
/rewind              # Navigate backward through history (or press Esc twice)
```

See [Checkpointing](https://geminicli.com/docs/cli/checkpointing/) and [Rewind](https://geminicli.com/docs/cli/rewind/).

## Sub-Agents & Remote Agents

Gemini can spawn specialized sub-agents for parallel task execution and coordinate with external remote agents:

- [Sub-Agents](https://geminicli.com/docs/core/subagents/)
- [Remote Agents](https://geminicli.com/docs/core/remote-agents/)

## Model Context Protocol (MCP)

Extend Gemini CLI with third-party tools and data sources via MCP:

```text
/mcp list            # List configured MCP servers
/mcp enable <name>
/mcp disable <name>
/mcp refresh         # Restart all servers
```

See [MCP Server setup](https://geminicli.com/docs/tools/mcp-server/).

## Hooks

Intercept and customize Gemini CLI behavior at specific lifecycle events:

```text
/hooks list          # Display all registered hooks
/hooks enable <name>
/hooks disable <name>
```

See [Hooks](https://geminicli.com/docs/hooks/) and [Writing Hooks](https://geminicli.com/docs/hooks/writing-hooks).

## Extensions

Install, manage, and build extensions to add custom tools and capabilities:

```text
/extensions list
/extensions install <repo-url>
/extensions enable <name>
/extensions disable <name>
```

See [Extensions](https://geminicli.com/docs/extensions/) and [Writing Extensions](https://geminicli.com/docs/extensions/writing-extensions/).

## IDE Integration

Connect Gemini CLI to your IDE for a companion coding experience:

```text
/ide status
/ide enable
/ide install
```

See the [IDE Integration guide](https://geminicli.com/docs/ide-integration/).

## Session Management

All conversations are automatically saved. Browse, resume, and manage sessions:

```text
/resume              # Browse previous sessions
/chat save <tag>     # Save a named checkpoint
/chat resume <tag>   # Resume from checkpoint
/chat share file.md  # Export conversation to file
```

## Additional Features

| Feature | Description | Link |
|---|---|---|
| Sandbox | Isolated execution environment | [Sandbox](https://geminicli.com/docs/cli/sandbox/) |
| Headless Mode | Non-interactive automation | [Headless](https://geminicli.com/docs/cli/headless/) |
| Token Caching | Reduce API costs | [Token Caching](https://geminicli.com/docs/cli/token-caching/) |
| Themes | Customize visual appearance | [Themes](https://geminicli.com/docs/cli/themes/) |
| Vim Mode | Vim-style input navigation | Use `/vim` to toggle |
| Custom Commands | User-defined prompt shortcuts | [Custom Commands](https://geminicli.com/docs/cli/custom-commands/) |

## Browser Agent

The Browser Agent is an experimental feature currently under active development. It automates web browser tasks—such as navigating websites, filling forms, clicking buttons, and extracting information from web pages—using the accessibility tree.
