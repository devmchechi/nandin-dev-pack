# My Work

Your representative on your team. Teams get work done by finding who is responsible for something, asking them, handing them work and following up. My Work does that with you, and answers for you when other people ask.

- **"Who's responsible for the SOX audit?"** It searches, live, what everyone connected to your Nandin relay publishes about themselves: their responsibilities, profile and agents. It says who matched, why, and whether they're online.
- **"Ask Lena for the SOC 1 evidence by Friday."** It finds Lena and writes the request. After you approve, it sends the request to Lena's Nandin, where her My Work answers or holds it for her.
- **"What am I waiting on?" / "What did people ask me?"** It lists open requests both ways, with status.
- **Questions about you.** When a teammate's agent asks "what does Dev own?", your My Work answers from your role and notes. Work someone assigns you waits for your approval.
- **Questions about your own work** ("What's due this week?") are answered from your notes, with sources.

## Set it up

1. **Your role.** Open the agent's Instructions tab and fill in `instructions.md`: title, team, what you own, recurring duties and who to escalate to.
2. **Your responsibilities, so others can find you.** In your `NANDIN.md` (Settings › Gateway, or the file in your agents repo), list them:
   ```yaml
   responsibilities: [CI/CD, AWS accounts, on-call rota, SOX IT controls]
   policy:
     require_approval: [assign-me]   # work assigned to you waits for you
   ```
   Your Nandin publishes these with your profile on the relay.
3. **Be reachable.** Turn the gateway on and connect to your team's relay. To share your `NANDIN.md` text as well, make your profile discoverable.
4. **Your notes (optional).** In Library › Tools › Filesystem › Setup, add your notes folder with the short name `my-work`, Read only. To try it, use `examples/my-work-notes/` from this pack.

Docker must be running.

## Example prompts

- "Who is responsible for Risk?"
- "List everyone on my network and what they own."
- "Ask the SOC 1 owner for last quarter's evidence."
- "Assign Sam: rotate the CI deploy keys by Friday."
- "What am I waiting on?"
- "What's due this week?"

## Capabilities in plain language

| Capability                       | Why                                                                                            |
| -------------------------------- | ---------------------------------------------------------------------------------------------- |
| Reads your network's profiles    | Finding who is responsible, from what people publish on your relay                             |
| Sends requests (asks first)      | Asking people and assigning work, each request approved by you                                 |
| Answers for you                  | Questions about your work (`ask-me`). Work assigned to you (`assign-me`) waits for your approval |
| Reads your shared notes          | The `my-work` folder, read only                                                                |
| Writes files or runs commands    | No                                                                                             |
