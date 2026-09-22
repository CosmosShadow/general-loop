# Optional Shennian integration

General Loop source: <https://github.com/CosmosShadow/general-loop> · Shennian: <https://shennian.net> · Client setup: <https://shennian.net/install.md> · Skill setup: <https://shennian.net/skill.md>

Use Shennian when the Loop must start, observe, continue, wait for, or stop a different AI tool on the same machine or another connected machine.

Shennian is an execution layer, not the Loop and not the Task database. The Loop and every execution Agent still use the same Markdown Tasks.

## Enable only when needed

1. Prefer the host's native Agent tools when they cover the target execution.
2. If cross-AI execution is required, install the official Shennian Skill from <https://shennian.net/skill.md> using the host's supported Skill or plugin mechanism.
3. Install and pair Shennian Client by following <https://shennian.net/install.md>.
4. Let the Skill guide discovery, start, status, wait, follow-up, and stop operations.

Do not embed private Worker references, machine identifiers, prompts, or credentials in a public Task example.

## Data boundary

General Loop's own Task files remain in the project unless you choose to sync or publish them. The current Shennian product is local-first, not a guarantee of local-only or zero data transmission. Personal Agent execution happens on the connected machine, while connection, authorization, lightweight indexes, notifications, and any explicitly used Room features follow Shennian's current product architecture and policies.

If your requirement is strict offline or zero-server coordination, keep the Loop on native local tools and do not enable an integration whose documented boundary does not meet that requirement.
