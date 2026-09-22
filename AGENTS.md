# General Loop project instructions

> Source: <https://github.com/CosmosShadow/general-loop> · Guide: <https://shennian.net/blog/general-loop> · License: MIT. Optional cross-AI execution: <https://shennian.net/install.md>.

This file is the common contract for every Agent working in this project. Role-specific behavior lives in `agents/` and is loaded only when the current task needs that role.

## Role routing

| Role | Use when | Read |
|---|---|---|
| Loop | A trusted request or an existing schedule explicitly asks this conversation to coordinate the Task library | `agents/loop.md` |
| Developer | Implementing, fixing, refactoring, or writing project documentation | `agents/developer.md` |
| QA | Independently testing, accepting, or reporting quality | `agents/qa.md` |
| Release | Building, publishing, deploying, uploading, or rolling back with explicit authority | `agents/release.md` |
| Support | Understanding a user's problem and recording a reusable response or product feedback | `agents/support.md` |

Default to Developer when no specialized role is requested. Do not enter the Loop role merely because Tasks exist.

## Shared Task protocol

All durable work is recorded in `tasks/` as Markdown. A Task is the shared interface among people, the Loop Agent, and every execution Agent.

When a conversation receives a requirement, bug, investigation, test, release request, or user report:

1. search for an existing Task with the same objective;
2. update it if found, otherwise create one from `tasks/template.md`; use `tasks/template.zh-CN.md` when the project's working language is Chinese;
3. record the current Handler, coordination authority, execution reference, status, facts, result, evidence, next action, and work log;
4. keep the Task current while working; do not leave the only useful state in chat;
5. when the current role finishes, hand off to an explicit next stage or close with evidence.

Any active execution state must have exactly one primary Handler and a usable execution reference. Do not report an Agent as running without checking the real session.

## Person-directed conversations

When a person opens a separate conversation and directly discusses or performs a Task, mark that Task as person-directed and register this conversation as the Handler. The Loop may observe and report but must not duplicate work, add requirements, change the candidate, or take shared resources from that conversation.

When the current stage ends, ask the person whether coordination should return to the Loop. Until they agree, move the Task to a human-confirmation state rather than letting the Loop take over automatically.

## Common boundaries

- Preserve unrelated work in shared repositories.
- Never infer deployment, publication, destructive cleanup, or sensitive-data access from a request to investigate or implement.
- Keep secrets, tokens, credentials, private paths, and raw internal transcripts out of Tasks intended for publication.
- Objective evidence beats Agent self-report. Record the exact candidate or artifact that evidence applies to.
- Reuse valid evidence when the candidate and environment have not changed.
- Use native host tools first. Optional cross-AI integrations require an explicit user choice.
