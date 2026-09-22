# Using General Loop with Codex

Codex can provide the complete minimum host when it can:

1. read the repository's `AGENTS.md` and role files;
2. create, message, inspect, and wait for other Codex tasks;
3. configure a recurring automation that wakes the same Loop conversation.

Open the project in Codex and say:

```text
You are the Loop role. Read AGENTS.md and agents/loop.md. Inspect tasks/ and
begin coordination. Configure a recurring wake-up for this same task.
```

Keep exactly one active Loop for one Task library. Execution Tasks may run in parallel when their files, candidates, devices, accounts, and release windows do not conflict.

Codex-native tools are enough for Codex execution Agents. Install an optional cross-AI integration only when you need another local AI tool that Codex cannot manage natively.
