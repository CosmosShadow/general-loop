# Other Agent hosts

General Loop does not require a specific model or vendor. A host needs:

- project instructions or a reliable way to load `AGENTS.md` and one role file;
- local file read/write access;
- tools for the work itself;
- a way to resume the same Loop context on a schedule;
- optionally, APIs or an integration for starting and observing other Agent sessions.

If a host uses a different instruction filename, create a thin adapter that points to `AGENTS.md`; do not fork the Task protocol into multiple divergent copies.

If the host cannot manage other sessions, it can still run a single-Agent Loop over the Task library. Cross-AI execution is an optional capability, not a requirement of the file protocol.
