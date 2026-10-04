
"{framework} configuration options" → customization
```

## Example: Creating a "Semantic Kernel" Skill

### Investigation

```
microsoft_docs_search(query="semantic kernel overview")
microsoft_docs_search(query="semantic kernel plugins functions")
microsoft_code_sample_search(query="semantic kernel", language="csharp")
microsoft_docs_fetch(url="https://learn.microsoft.com/semantic-kernel/overview/")
```

### Generated Skill

```
semantic-kernel/
├── SKILL.md
└── sample_codes/
    ├── getting-started/
    │   └── hello-kernel.cs
    └── common-patterns/
        ├── chat-completion.cs
        └── function-calling.cs
```

### Generated SKILL.md

```markdown
---
name: semantic-kernel
description: Build AI agents with Microsoft Semantic Kernel. Use for LLM-powered apps with plugins, planners, and memory in .NET or Python.
---

# Semantic Kernel

Orchestration SDK for integrating LLMs into applications with plugins, planners, and memory.

## Key Concepts

- **Kernel**: Central orchestrator managing AI services and plugins
- **Plugins**: Collections of functions the AI can call
- **Planner**: Sequences plugin functions to achieve goals
- **Memory**: Vector store integration for RAG patterns

## Quick Start

See [getting-started/hello-kernel.cs](sample_codes/getting-started/hello-kernel.cs)

## Learn More

| Topic | How to Find |
|-------|-------------|
| Plugin development | `microsoft_docs_search(query="semantic kernel plugins custom functions")` |
| Planners | `microsoft_docs_search(query="semantic kernel planner")` |
| Memory | `microsoft_docs_fetch(url="https://learn.microsoft.com/en-us/semantic-kernel/frameworks/agent/agent-memory")` |

## CLI Alternative

If the Learn MCP server is not available, use the `mslearn` CLI instead:

| MCP Tool | CLI Command |
|----------|-------------|
| `microsoft_docs_search(query: "...")` | `mslearn search "..."` |
| `microsoft_code_sample_search(query: "...", language: "...")` | `mslearn code-search "..." --language ...` |
| `microsoft_docs_fetch(url: "...")` | `mslearn fetch "..."` |

Run directly with `npx @microsoft/learn-cli <command>` or install globally with `npm install -g @microsoft/learn-cli`.
```
