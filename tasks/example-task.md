# [testing] Prevent duplicate background jobs

Status: testing  
Task ID: TASK-EXAMPLE-001  
Source: user report  
Current Handler: QA Agent B  
Execution role: QA  
Coordination authority: Loop-managed  
Execution reference: test-session-b  
Last activity: focused unit tests passed; QA is reproducing the original race on the fixed candidate  
Result: implementation complete, independent verification pending  
Next action: QA Agent B runs the two-process reproduction against commit `example123`

## Objective and acceptance criteria

Starting the same job twice must produce one active worker and one safe no-op. Existing single-worker behavior must remain unchanged.

## Confirmed facts, unknowns, and risks

- The race occurs only when two processes acquire the old lock within the same second.
- The candidate uses an atomic lock-file create.
- Shared test port 4310 is reserved by QA Agent B for this run.

## Current execution

- Candidate or artifact: commit `example123`
- Environment and shared resources: local test fixture; port 4310
- Live status: testing
- Current blocker: none
- Recovery or continuation method: continue `test-session-b`

## Result and evidence

- Developer: focused lock tests passed on `example123`.
- QA: pending independent two-process reproduction.

## Human decision required

None.

## Work log

- 2026-01-01 09:00 | Support Agent | recorded user reproduction | waiting for triage
- 2026-01-01 09:10 | Loop Agent | assigned Developer Agent A | waiting for development → developing
- 2026-01-01 10:20 | Developer Agent A | produced candidate and focused evidence | developing → waiting for test
- 2026-01-01 10:30 | Loop Agent | assigned independent QA and reserved port | waiting for test → testing
