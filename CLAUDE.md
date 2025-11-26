# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a documentation-only repository containing a comprehensive guide of ~30 pro tips for using Gemini CLI (Google's open-source AI assistant for the command line). The entire content lives in a single `README.md` file.

## Claude Agent Ecosystem for Gemini CLI

This repository includes a complete Claude agent ecosystem for autonomously operating Gemini CLI:

### Quick Usage

**🚀 POWER Agent** (natural language → extraordinary results):
```
/gemini-power Build me a full-stack e-commerce app with React, Node, and Postgres
/gemini-power Make this codebase production ready
/gemini-power Find and fix all security vulnerabilities
/gemini-power I have a bug somewhere, the app crashes under load
/gemini-power Migrate this from JavaScript to TypeScript
```

**Setup Agent** (run first on new systems):
```
/gemini-setup                           # Full environment setup
/gemini-setup Configure for CI/CD       # CI-specific setup
```

**Standard Operator Agent** (direct task execution):
```
/gemini Create a Python FastAPI server with user authentication
/gemini Debug the connection errors in ./logs/error.log
```

### Agent Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                 Natural Language Request                     │
│    "Make this production ready" / "Fix everything"          │
└─────────────────────────────────────────────────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────┐
│            🚀 GEMINI POWER Agent (gemini-power)              │
│                                                              │
│  COGNITIVE LAYER:                                            │
│  • Intent Recognition (what do they really want?)           │
│  • Task Classification (GENESIS/DETECTIVE/SURGEON/etc.)     │
│  • Complexity Assessment (trivial → legendary)              │
│                                                              │
│  PROTOCOL LIBRARY:                                           │
│  • GENESIS    - Create from scratch                         │
│  • DETECTIVE  - Debug and fix bugs                          │
│  • SURGEON    - Refactor and improve                        │
│  • SENTINEL   - Security hardening                          │
│  • ARCHITECT  - Infrastructure/DevOps                       │
│  • TRANSFORMER- Migrations/modernization                    │
│  • GUARDIAN   - Testing and quality                         │
│  • SCHOLAR    - Documentation/understanding                 │
│  • OMNIBUS    - Complete transformation                     │
│                                                              │
│  EXECUTION ENGINE:                                           │
│  • Multi-phase orchestration                                │
│  • Self-healing error recovery                              │
│  • Session management for epic tasks                        │
│  • Verification at every step                               │
└─────────────────────────────────────────────────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                    Gemini CLI Execution                      │
│  gemini --checkpointing -p "..."                            │
└─────────────────────────────────────────────────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────┐
│              ✅ Verified, Tested, Documented                 │
└─────────────────────────────────────────────────────────────┘
```

### Agent Files

**Slash Commands (Claude Code)**
- `.claude/commands/gemini-power.md` - 🚀 **POWER agent** for extraordinary tasks
- `.claude/commands/gemini.md` - Standard operator agent
- `.claude/commands/gemini-setup.md` - Setup agent for environment configuration

**System Prompts (Standalone Deployment)**
- `agents/gemini-power-agent-system-prompt.md` - 🚀 **Full POWER agent system prompt**
- `agents/claude-gemini-agent-system-prompt.md` - Operator agent system prompt
- `agents/claude-gemini-setup-agent-system-prompt.md` - Setup agent system prompt

**Reference Documentation**
- `agents/gemini-cli-operator.md` - Comprehensive operational guide

### Power Agent Protocols

| Protocol | Triggers | What It Does |
|----------|----------|--------------|
| **GENESIS** | "create", "build", "make" | Full-stack app generation with tests |
| **DETECTIVE** | "fix", "debug", "broken" | Root cause analysis + surgical fix |
| **SURGEON** | "refactor", "improve", "clean" | Code quality transformation |
| **SENTINEL** | "secure", "audit", "vulnerability" | OWASP Top 10 + CVE scanning |
| **ARCHITECT** | "deploy", "docker", "k8s", "CI/CD" | Infrastructure as code |
| **TRANSFORMER** | "migrate", "upgrade", "modernize" | Large-scale codebase evolution |
| **GUARDIAN** | "test", "coverage" | 80%+ coverage generation |
| **SCHOLAR** | "explain", "document" | Architecture docs + diagrams |
| **OMNIBUS** | "everything", "production ready" | All protocols chained |

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
