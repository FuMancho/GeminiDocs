# Commands Reference

Complete reference for all Gemini CLI commands. Commands are prefixed with `/` (slash commands), `@` (at-commands for file injection), or `!` (shell passthrough).

## Slash Commands

### Session & Navigation

| Command | Description |
|---|---|
| `/help` (`/?`) | Show available commands |
| `/quit` (`/exit`) | Exit Gemini CLI |
| `/clear` | Clear terminal display (`Ctrl+L`) |
| `/resume` | Browse and resume previous sessions |
| `/rewind` | Navigate backward through history (`Esc` × 2) |
| `/restore [id]` | Restore project files to a checkpoint |

### Conversation Management

| Command | Description |
|---|---|
| `/chat save <tag>` | Save current conversation state |
| `/chat resume <tag>` | Resume from a saved checkpoint |
| `/chat list` | List saved checkpoints (project-scoped) |
| `/chat delete <tag>` | Delete a saved checkpoint |
| `/chat share [file]` | Export conversation to `.md` or `.json` |
| `/chat debug` | Export the most recent API request as JSON |
| `/compress` | Replace chat context with a summary (saves tokens) |
| `/copy` | Copy last output to clipboard |

### Configuration & Settings

| Command | Description |
|---|---|
| `/settings` | Open the interactive settings editor |
| `/model manage` | Configure the model interactively |
| `/model set <name> [--persist]` | Set the active model |
| `/theme` | Change the visual theme |
| `/editor` | Select a supported editor |
| `/vim` | Toggle vim-style input navigation |
| `/terminal-setup` | Configure terminal keybindings for multiline input |
| `/auth` | Change authentication method |
| `/privacy` | Display privacy notice and consent options |
| `/permissions trust [dir]` | Manage folder trust settings |

### Tools & Extensions

| Command | Description |
|---|---|
| `/tools [desc]` | List available tools (add `desc` for descriptions) |
| `/mcp list` | List configured MCP servers |
| `/mcp enable <name>` | Enable an MCP server |
| `/mcp disable <name>` | Disable an MCP server |
| `/mcp refresh` | Restart all MCP servers |
| `/mcp auth <name>` | Authenticate with an OAuth-enabled MCP server |
| `/extensions list` | List active extensions |
| `/extensions install <repo>` | Install an extension |
| `/extensions enable <name>` | Enable an extension |
| `/extensions disable <name>` | Disable an extension |
| `/extensions update [--all]` | Update extensions |

### Agent Features

| Command | Description |
|---|---|
| `/skills list` | List all discovered skills |
| `/skills enable <name>` | Enable a skill |
| `/skills disable <name>` | Disable a skill |
| `/skills reload` | Refresh skills from all tiers |
| `/hooks list` | Display all registered hooks |
| `/hooks enable <name>` | Enable a hook |
| `/hooks disable <name>` | Disable a hook |
| `/plan` | Switch to Plan Mode (read-only) |
| `/policies list` | List all active policies by mode |

### Workspace & Files

| Command | Description |
|---|---|
| `/directory add <path>` | Add a directory to the workspace |
| `/directory show` | Display all added directories |
| `/init` | Generate a `GEMINI.md` context file for the project |
| `/memory add <text>` | Add text to AI memory |
| `/memory list` | List active `GEMINI.md` file paths |
| `/memory refresh` | Reload memory from all `GEMINI.md` files |
| `/memory show` | Display the full concatenated memory |
| `/commands reload` | Reload custom command definitions |

### Other

| Command | Description |
|---|---|
| `/about` | Show version info |
| `/bug [title]` | File a bug report on GitHub |
| `/docs` | Open documentation in browser |
| `/ide status` | Check IDE integration status |
| `/shells` (`/bashes`) | Toggle background shells view |
| `/setup-github` | Set up GitHub Actions with Gemini |
| `/stats session` | Show session usage statistics |
| `/stats model` | Show model token/quota info |
| `/stats tools` | Show tool usage statistics |

## At Commands (`@`)

Inject file or directory contents directly into your prompt:

```text
@path/to/file.txt Explain this code.
@src/                Summarize all files in this directory.
```

> [!TIP]
> Git-ignored files (e.g., `node_modules/`, `.env`) are excluded by default. Configure this via the `context.fileFiltering` setting.

## Shell Passthrough (`!`)

Prefix a command with `!` to run it directly in your shell without leaving Gemini CLI:

```text
!git status
!npm test
```

## Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Ctrl+L` | Clear screen |
| `Esc` × 2 | Rewind |
| `Alt+Z` / `Cmd+Z` | Undo in input |
| `Shift+Alt+Z` / `Shift+Cmd+Z` | Redo in input |
