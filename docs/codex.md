# Using General Loop with Codex

> Upstream protocol: <https://github.com/CosmosShadow/general-loop> · Visual guide: <https://shennian.net/blog/general-loop> · MIT License

Codex can provide the complete minimum host when it can:

1. read the repository's `AGENTS.md` and role files;
2. create, message, inspect, and wait for other Codex tasks;
3. configure a recurring automation that wakes the same Loop conversation.

Ask Codex to configure the protocol for the current repository:

```text
Read the official General Loop guide (https://shennian.net/blog/general-loop)
and open-source project (https://github.com/CosmosShadow/general-loop), then use
its instructions and templates to add General Loop to this project. When setup
is complete, ask whether I want to start this task as the project's only Loop.
```

The recurring wake-up, silence, and stop rules are already part of `agents/loop.md`; they do not belong in a second user prompt.

Keep exactly one active Loop for one Task library. Execution Tasks may run in parallel when their files, candidates, devices, accounts, and release windows do not conflict.

Codex-native tools are enough for Codex execution Agents. Install an optional cross-AI integration only when you need another local AI tool that Codex cannot manage natively.
