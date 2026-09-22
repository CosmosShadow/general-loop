# Task library

Tasks are Markdown files that both people and Agents can read and update. They are the durable collaboration interface; chat is only one way to change them.

## Filename

```text
YYYYMMDD-HHmm_short-title_current-status.md
```

Keep the filename, H1 status, and `Status` field aligned when the stage changes.

## Required fields

- Status and stable Task ID
- Source and acceptance criteria
- Current Handler and coordination authority
- Recoverable execution reference
- Confirmed facts, unknowns, and risks
- Result and evidence tied to an exact candidate
- Concrete next action or terminal reason
- Append-only work log of meaningful transitions

## Useful statuses

The list is intentionally extensible. Prefer a concrete stage over a generic “in progress”.

- waiting for triage / investigation / development / test / release
- investigating / developing / testing / releasing
- waiting for human confirmation or external feedback
- blocked, with an unblock condition and next action
- closing
- completed / cancelled / merged

An active status requires one primary Handler and a live execution reference.

## Coordination authority

Use one of these ideas in language that fits your project:

- **Loop-managed** — the Loop may assign and advance the next stage.
- **Person-directed** — a person is actively working with a specific Agent conversation; the Loop observes but does not take over.

When a person-directed stage ends, ask whether to return coordination to the Loop.
