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

## User-triggered tools

You can directly trigger these tools using special syntax in your prompts.

- **File access (`@`)**: Use the `@` symbol followed by a file or directory path to include its content in your prompt. This triggers the `read_many_files` tool.
- **Shell commands (`!`)**: Use the `!` symbol followed by a system command to execute it directly. This triggers the `run_shell_command` tool.

## Model-triggered tools

The Gemini model automatically requests these tools when it needs to perform specific actions or gather information to fulfill your requests. You do not call these tools manually.

### File management

These tools let the model explore and modify your local codebase.

- **Directory listing (`list_directory`)**: Lists files and subdirectories.
- **File reading (`read_file`)**: Reads the content of a specific file.
- **File writing (`write_file`)**: Creates or overwrites a file with new content.
- **File search (`glob`)**: Finds files matching a glob pattern.
- **Text search (`search_file_content`)**: Searches for text within files using grep or ripgrep.
- **Text replacement (`replace`)**: Performs precise edits within a file.

### Agent coordination

These tools help the model manage its plan and interact with you.

- **Ask user (`ask_user`)**: Requests clarification or missing information from you via an interactive dialog.
- **Memory (`save_memory`)**: Saves important facts to your long-term memory (`GEMINI.md`).
- **Subtasks (`write_tasks`)**: Manages a list of subtasks for complex plans.
- **Agent Skills (`activate_skill`)**: Loads specialized procedural expertise when needed.
- **Browser agent (`browser_agent`)**: Automates web browser tasks through the accessibility tree.
- **Internal docs (`get_internal_docs`)**: Accesses Gemini CLI's own documentation to help answer your questions.

### Information gathering

These tools provide the model with access to external data.

- **Web fetch (`web_fetch`)**: Retrieves and processes content from specific URLs.
- **Web search (`google_web_search`)**: Performs a Google Search to find up-to-date information.

## How to use tools

You use tools indirectly by providing natural language prompts to Gemini CLI.

1. **Prompt**: You enter a request or use syntax like `@` or `!`.
2. **Request**: The model analyzes your request and identifies if a tool is required.
3. **Validation**: If a tool is needed, the CLI validates the parameters and checks your security settings.
4. **Confirmation**: For sensitive operations (like writing files), the CLI prompts you for approval.
5. **Execution**: The tool runs, and its output is sent back to the model.
6. **Response**: The model uses the results to generate a final, grounded answer.

## Security and confirmation

Safety is a core part of the tool system. To protect your system, Gemini CLI implements several safeguards.

- **User confirmation**: You must manually approve tools that modify files or execute shell commands. The CLI shows you a diff or the exact command before you confirm.
- **Sandboxing**: You can run tool executions in secure, containerized environments to isolate changes from your host system.
- **Trusted folders**: You can configure which directories allow the model to use system tools.

Always review confirmation prompts carefully before allowing a tool to execute.
