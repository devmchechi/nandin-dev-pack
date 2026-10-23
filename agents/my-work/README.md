# My Work

Answers questions about your own job: what you own, who to ask, what's due and how your team does things. It reads only two things: your **instructions** (your role, in `instructions.md`) and a **notes folder** you share with it read-only. Every answer ends with the files it came from. When your notes don't say, it tells you, and suggests where to add it.

## What it needs

1. **A notes folder.** Any folder of Markdown or text files: responsibilities, owners, contacts, on-call, deadlines, runbooks, decisions. Subfolders are fine.
2. **Share it as `my-work`.** In Library › Tools › Filesystem › Setup, choose **Add a folder**, pick the folder, set the short name to `my-work` and access to **Read only**, then **Save settings**.
3. **Your role.** Open the agent's Instructions tab and fill in `instructions.md`: title, team, what you own, recurring duties and who to escalate to.

Docker must be running: the agent's tools run in its container.

To try it without your own notes, share `examples/my-work-notes/` from this pack as `my-work`.

## Example prompts

- "What do I own?"
- "Who do I escalate a security issue to?"
- "What's due this week?"
- "What's the on-call handover process?"
- "Who approves production deploys?"

## Capabilities in plain language

| Capability                   | Why                                                 |
| ---------------------------- | --------------------------------------------------- |
| Reads your shared notes      | The `my-work` folder, read only                     |
| Reads files in its own folder | Its working folder, if you put notes there instead |
| Writes files                 | No                                                  |
| Runs commands                | No                                                  |
| Network                      | None                                                |
