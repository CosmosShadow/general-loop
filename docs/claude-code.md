# Using General Loop with Claude Code

> Upstream protocol: <https://github.com/CosmosShadow/general-loop> · Visual guide: <https://shennian.net/blog/general-loop> · MIT License

`CLAUDE.md` points Claude Code to the common `AGENTS.md` contract. First configure the protocol without assigning the current conversation as Loop:

```text
Read the official General Loop guide (https://shennian.net/blog/general-loop)
and open-source project (https://github.com/CosmosShadow/general-loop), then add
General Loop to this project. Configure the required AGENTS.md, agents/, and
tasks/ for the current project structure, then ask whether I want this
conversation to become the project's only Loop and begin coordination now.
```

Optionally start coordination with a separate instruction:

```text
Yes. Make this conversation the project's only Loop and begin coordinating all
existing Tasks now. Prefer a native recurring wake-up every five minutes. If no
scheduler exists but this conversation can safely wait and resume, wait five
minutes after each complete cycle and continue until I pause it or every Task is
terminal; otherwise explain that an external wake-up mechanism is required.
```

Claude Code needs a recurring wake-up mechanism for unattended coordination. Use its supported scheduling mechanism when available, or an external scheduler that re-enters the same Loop context. The scheduler should wake the Loop; it should not contain a second copy of the project's decision logic.

If the Loop needs to control other AI tools, see the optional Shennian integration.
