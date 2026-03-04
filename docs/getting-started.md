# Getting Started with Gemini CLI

Gemini CLI brings the power of Google's advanced language models directly to your terminal. It helps you understand code, generate solutions, manage files, and automate workflows from the command line.

## Prerequisites

- **Node.js 18+** and **npm** installed.
- A **Google account** for authentication.

> [!NOTE]
> Certain Google Cloud or enterprise account types may require additional project configuration. See the [Authentication Guide](https://geminicli.com/docs/get-started/authentication/) for details.

## Installation

Install Gemini CLI globally via npm:

```bash
npm install -g @google/gemini-cli
```

For additional installation options, see the [Installation Guide](https://geminicli.com/docs/get-started/installation/).

## Authenticate

To begin using Gemini CLI, you must authenticate with a Google service. In most cases, you can log in with your existing Google account:

1. Run Gemini CLI after installation:

   ```bash
   gemini
   ```

2. When asked "How would you like to authenticate for this project?" select **1. Login with Google**.
3. Select your Google account.
4. Click on **Sign in**.

Certain account types may require you to configure a Google Cloud project. For more information, including other authentication methods, see [Gemini CLI Authentication Setup](https://geminicli.com/docs/get-started/authentication/).

## Configure

Gemini CLI offers several ways to configure its behavior, including environment variables, command-line arguments, and settings files.

To explore your configuration options, see [Gemini CLI Configuration](https://geminicli.com/docs/reference/configuration/).

## Use

Once installed and authenticated, you can start using Gemini CLI by issuing commands and prompts in your terminal. Ask it to generate code, explain files, and more.

To explore the power of Gemini CLI, see [Gemini CLI examples](https://geminicli.com/docs/get-started/examples/).

## Check Usage & Quota

Monitor your token usage and quota with:

```text
/stats model
```

## Essential Commands

| Command | Description |
|---|---|
| `/help` or `/?` | Show available commands |
| `/clear` | Clear the terminal display |
| `/settings` | Open the configuration editor |
| `/model set <name>` | Switch the active model |
| `/chat save <tag>` | Save current conversation state |
| `/chat resume <tag>` | Resume a saved conversation |
| `/resume` | Browse and resume previous sessions |
| `/plan` | Switch to Plan Mode (read-only) |
| `/quit` or `/exit` | Exit Gemini CLI |

See the full [Commands Reference](./commands.md) for all slash commands, at-commands, and shortcuts.

## What's Next?

- [Gemini CLI Examples](https://geminicli.com/docs/get-started/examples/) — See what Gemini CLI can do
- [Configuration](https://geminicli.com/docs/reference/configuration/) — Customize behavior and settings
- [Tutorials](https://geminicli.com/docs/cli/tutorials/file-management/) — Step-by-step guides
- [Extensions](https://geminicli.com/docs/extensions/) — Extend Gemini CLI with plugins
