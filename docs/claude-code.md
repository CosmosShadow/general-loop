# Using General Loop with Claude Code

> Upstream protocol: <https://github.com/CosmosShadow/general-loop> · Visual guide: <https://shennian.net/blog/general-loop> · MIT License

`CLAUDE.md` points Claude Code to the common `AGENTS.md` contract. Configure the protocol with one prompt:

```text
Read the official General Loop guide (https://shennian.net/blog/general-loop)
and open-source project (https://github.com/CosmosShadow/general-loop), then use
its instructions and templates to add General Loop to this project. When setup
is complete, ask whether I want to start this conversation as the project's only
Loop.
```

The recurring wake-up and wait-and-resume behavior are already defined in `agents/loop.md`; they do not belong in a second user prompt.

Claude Code needs a recurring wake-up mechanism for unattended coordination. Use its supported scheduling mechanism when available, or an external scheduler that re-enters the same Loop context. The scheduler should wake the Loop; it should not contain a second copy of the project's decision logic.

If the Loop needs to control other AI tools, see the optional Shennian integration.
