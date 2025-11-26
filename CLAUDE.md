# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a documentation-only repository containing a comprehensive guide of ~30 pro tips for using Gemini CLI (Google's open-source AI assistant for the command line). The entire content lives in a single `README.md` file.

## Claude Agent Ecosystem for Gemini CLI

This repository includes a complete Claude agent ecosystem for autonomously operating Gemini CLI:

### Quick Usage

**Setup Agent** (run first on new systems):
```
/gemini-setup                           # Full environment setup
/gemini-setup Configure for CI/CD       # CI-specific setup
/gemini-setup Add Python project context # Project-specific setup
```

**Operator Agent** (execute tasks):
```
/gemini Create a Python FastAPI server with user authentication
/gemini Debug the connection errors in ./logs/error.log
/gemini Refactor ./src/api/ to use async/await patterns
```

### Agent Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    User Request                              │
└─────────────────────────────────────────────────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────┐
│              Setup Agent (gemini-setup)                      │
│  • Install Gemini CLI                                       │
│  • Configure authentication                                  │
│  • Create GEMINI.md context files                           │
│  • Set up custom commands                                   │
│  • Install extensions                                       │
│  • Verify environment readiness                             │
└─────────────────────────────────────────────────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────┐
│              Operator Agent (gemini)                         │
│  • Analyze task requirements                                │
│  • Select optimal Gemini CLI approach                       │
│  • Execute commands (headless or interactive)               │
│  • Manage context and sessions                              │
│  • Verify results                                           │
│  • Handle errors and recovery                               │
└─────────────────────────────────────────────────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                    Task Completed                            │
└─────────────────────────────────────────────────────────────┘
```

### Agent Files

**Slash Commands (Claude Code)**
- `.claude/commands/gemini.md` - Operator agent for executing tasks
- `.claude/commands/gemini-setup.md` - Setup agent for environment configuration

**System Prompts (Standalone Deployment)**
- `agents/claude-gemini-agent-system-prompt.md` - Full operator agent system prompt
- `agents/claude-gemini-setup-agent-system-prompt.md` - Full setup agent system prompt

**Reference Documentation**
- `agents/gemini-cli-operator.md` - Comprehensive operational guide and decision framework

## Content Structure

The README covers:
- Getting started with Gemini CLI (installation via npm, authentication)
- Configuration tips (GEMINI.md context files, settings.json, custom slash commands)
- Extension mechanisms (MCP servers, extensions)
- Productivity features (memory, checkpointing, session management, compression)
- IDE integration (VS Code)
- Automation (GitHub Actions, headless/scripting mode)
- Advanced topics (multimodal AI, telemetry, custom PATH, YOLO mode)

## Working with This Repository

Since this is documentation-only:
- There are no build, test, or lint commands
- Changes should maintain the existing Markdown formatting style
- Each tip follows a consistent pattern: quick use-case summary followed by detailed explanation
- Code blocks use appropriate language hints (bash, json, markdown)
- External links use inline reference format with source citations
