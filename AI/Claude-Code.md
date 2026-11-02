![alt text](image-1.png)

# Claude Code: Developer Reference & Cheat Sheet

Claude Code is an agentic command-line tool developed by Anthropic. It runs directly in your terminal, inspects your codebase, edits files, executes shell commands, handles Git workflows, and automates daily development tasks.

---

## 1. Quick Start & Installation

### Installation Commands

```bash
# macOS / Linux / WSL (Recommended via installer)
curl -fsSL https://claude.ai/install.sh | bash

# macOS via Homebrew
brew install --cask claude-code

# Node.js / npm (Requires Node.js v18+)
npm install -g @anthropic-ai/claude-code

# Windows PowerShell
irm https://claude.ai/install.ps1 | iex

```

### Initializing & Authenticating

```bash
# Start an interactive session in your project root
cd /path/to/your/project
claude

# Authenticate via browser prompt or export your key directly
export ANTHROPIC_API_KEY="sk-ant-api03-..."

```

---

## 2. Basic Command-Line Usage

```bash
# Start interactive prompt mode
claude

# Execute a one-shot query without staying in the session
claude -p "Explain the data flow in src/services/auth.ts"

# Continue the previous conversation session
claude --continue

# Pass piped input or logs to Claude
git diff | claude -p "Review these changes for edge cases or bugs"

# Specify a custom model
claude --model claude-3-7-sonnet

```

---

## 3. Built-In Interactive Commands

When running inside an active `claude` session, use these core slash commands:

| Command | Action |
| --- | --- |
| `/help` | Show available slash commands and settings |
| `/clear` | Clear conversation history from the current session |
| `/compact` | Compact the context window to free up memory |
| `/status` | View current configuration, active model, and session metadata |
| `/cost` | Display token usage and estimated API cost for the current session |
| `/review` | Review recent file edits made by Claude before committing |
| `/model` | Switch the active Claude model (e.g., Sonnet, Opus, Haiku) |
| `/fast` | Toggle fast mode on/off for quicker iterations |
| `/bug` | Report an issue or unexpected behavior to Anthropic |

---

## 4. Project Configuration (`CLAUDE.md`)

Place a `CLAUDE.md` file in your repository's root directory. Claude Code reads this file at the start of every session to align with your team's project conventions and workflows.

### Example `CLAUDE.md` Setup

```markdown
# Project Instructions & Coding Guidelines

## Build & Test Commands
- Build project: `npm run build`
- Run unit tests: `npm test`
- Run single test file: `npx jest src/components/Button.test.tsx`
- Lint code: `npm run lint`

## Code Style & Conventions
- Use TypeScript with strict mode enabled.
- Prefer functional components and hooks for React code.
- Avoid using `any`; define explicit types or interfaces.
- Handle errors using custom `AppError` exceptions in backend services.

## Architecture Guidelines
- Business logic belongs in `src/services/`, not API handlers.
- UI components live in `src/components/` with companion `.test.tsx` files.

```

---

## 5. Common Developer Workflows

### Feature Implementation & Bug Fixing

```bash
# Implement a feature based on a description
claude "Add a rate limiting middleware to src/server.ts using express-rate-limit"

# Fix bugs using trace logs
claude "I'm getting a NullPointerException in UserService.java when creating a user. Fix it."

```

### Refactoring & Code Reviews

```bash
# Refactor messy functions
claude -p "Refactor src/utils/formatters.ts to improve readability and type safety"

# Code review ahead of PR submission
claude -p "Review uncommitted git changes and suggest improvements or security fixes"

```

### Git & Pull Request Automation

```bash
# Auto-generate a git commit message and commit
claude "Commit my staged changes with a concise, conventional commit message"

# Create a pull request automatically
claude "Create a PR branch, push changes, and open a PR with summary notes"

```

---

## 6. Model Context Protocol (MCP) Integration

Claude Code supports MCP, enabling connection to local or remote tools, external databases, and APIs.

### Configuring MCP Tools (`~/.claude.json` or `.claude/mcp.json`)

```json
{
  "mcpServers": {
    "postgres": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-postgres", "postgresql://localhost/mydb"]
    },
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "ghp_your_token_here"
      }
    }
  }
}

```

---

## 7. Advanced Configuration (`settings.json`)

Customize global or project settings via `.claude/settings.json`.

```json
{
  "$schema": "https://json.schemastore.org/claude-code-settings.json",
  "model": "claude-3-7-sonnet",
  "autoCompactEnabled": true,
  "autoCompactWindow": 0.8,
  "alwaysThinkingEnabled": true,
  "fastMode": false,
  "language": "english"
}

```

---

## 8. Keyboard Shortcuts & Terminal Tips

* `Ctrl + C`: Cancel current Claude response generation or tool execution.
* `Tab`: Auto-complete file paths and interactive commands.
* `Esc`: Clear input line or break out of current prompt block.
* Piped input: `cat error.log | claude -p "Analyze this stack trace"`.