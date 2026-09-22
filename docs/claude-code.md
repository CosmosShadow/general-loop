# Using General Loop with Claude Code

`CLAUDE.md` points Claude Code to the common `AGENTS.md` contract. Start the Loop by explicitly assigning the role:

```text
You are the Loop role for this project. Read CLAUDE.md, AGENTS.md, and
agents/loop.md, then inspect tasks/ and begin coordination.
```

Claude Code needs a recurring wake-up mechanism for unattended coordination. Use its supported scheduling mechanism when available, or an external scheduler that re-enters the same Loop context. The scheduler should wake the Loop; it should not contain a second copy of the project's decision logic.

If the Loop needs to control other AI tools, see the optional Shennian integration.
