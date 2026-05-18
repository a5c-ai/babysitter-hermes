# babysitter

Orchestrate complex, multi-step workflows with event-sourced state management, hook-based extensibility, and human-in-the-loop approval

## Prerequisites

Install the Babysitter CLI once. The `babysitter` command is backed by the SDK and exposes the canonical harness/plugin installer used in tests:

```bash
npm install -g @a5c-ai/babysitter
```

## Installation — Hermes

```bash
npm install -g @a5c-ai/babysitter-hermes
babysitter-hermes install --global
```

Restart Hermes to pick up the installed plugin.

For scriptable installs, prefer the SDK helper shape:

```bash
babysitter harness:install-plugin <harness>
babysitter harness:install-plugin <harness> --workspace /path/to/repo
```

## What's Included

- **Skills**: babysit
- **Hooks**: PostToolUse
- **Commands**: (directory)

- **CLI**: Install/uninstall scripts for global and workspace setup



## Verification

```bash
babysitter harness:discover --json | grep hermes
```

## Integration Model

The plugin provides:

- Core orchestration skill for multi-step workflow management
- Lifecycle hooks for session state, orchestration loops, and token compression
- Command wrappers for plan, resume, doctor, and other operations

The process library is fetched and bound through the SDK CLI.
