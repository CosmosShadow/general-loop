# Using General Loop with Codex

> Upstream protocol: <https://github.com/CosmosShadow/general-loop> · Visual guide: <https://shennian.net/blog/general-loop> · MIT License

Codex can provide the complete minimum host when it can:

1. read the repository's `AGENTS.md` and role files;
2. create, message, inspect, and wait for other Codex tasks;
3. configure a recurring automation that wakes the same Loop conversation.

First ask Codex to configure the protocol for the current repository:

```text
Read the official General Loop guide (https://shennian.net/blog/general-loop)
and open-source project (https://github.com/CosmosShadow/general-loop), then add
General Loop to this project. Configure the required AGENTS.md, agents/, and
tasks/ for the current project structure, then ask whether I want this task to
become the project's only Loop and begin coordination now.
```

When you want this task to become the active Loop, optionally say:

```text
Yes. Make this task the project's only Loop and begin coordinating all existing
Tasks now. Configure a native recurring wake-up every five minutes. Stay quiet
when nothing changes and continue until I pause it or every Task is terminal.
```

Keep exactly one active Loop for one Task library. Execution Tasks may run in parallel when their files, candidates, devices, accounts, and release windows do not conflict.

Codex-native tools are enough for Codex execution Agents. Install an optional cross-AI integration only when you need another local AI tool that Codex cannot manage natively.
